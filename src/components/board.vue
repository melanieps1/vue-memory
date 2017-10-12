<template>
	
	<div class="board">

		<card
					v-for="(card, index) in deck.cards"
					v-bind:face=card.face
					v-bind:showing=card.showing
					v-bind:index=index
					v-bind:flippable=card.flippable
					v-bind:flips="flipped.length"
					v-on:flipCard="flipCard">
			</card>

	</div>

</template>


<script>

import card from './card.vue'

export default {
	name: 'board',

	components: {
		card
	},

	data:  function() {
		return {
			turn: 0,      // turn number
			pairs: 0,     // number of matched made
			flipped: [],  // number of cards that are flipped in this turn

			deck: {
				cards: [
					{
						face: 'A',
						showing: false,
						flippable: true
					},
					{
						face: 'B',
						showing: false,
						flippable: true
					},
					{
						face: 'B',
						showing: false,
						flippable: true
					},
					{
						face: 'A',
						showing: false,
						flippable: true
					}
				]
			}
		}

	},

	methods: {

		noMatchThisTurn: function() {
			this.deck.cards[this.flipped[0]].flippable = true;
			this.deck.cards[this.flipped[0]].showing = false;
			this.deck.cards[this.flipped[1]].flippable = true;
			this.deck.cards[this.flipped[1]].showing = false;
			this.turn++;
			this.flipped = [];
		},

		flipCard: function(index) {
			// alert('flip card' + uid);
			this.deck.cards[index].showing = !this.deck.cards[index].showing;
			this.deck.cards[index].flippable = false;
			this.flipped.push(index);
			if (this.flipped.length == 2) {

				// check to see if flipped cards match				
				if (this.deck.cards[this.flipped[0]].face === this.deck.cards[this.flipped[1]].face) {

					// we have a match!
					this.turn++;
					this.pairs++;
					this.flipped = [];

					// check for win
					if (this.deck.cards.length/2 === this.pairs) {
						// game is won!
						alert('you won!')
					}
				} else {
					console.log('not a match, resetting cards');

					// not a match, wait five seconds then turn cards back over
					setTimeout(this.noMatchThisTurn, 2000);
				}
			}
		}

	}
	
}
	
</script>


<style>
	
</style>