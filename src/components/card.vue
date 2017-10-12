<template>

	<div class="card"
		v-bind:class="{ 'back': !showing }"
		v-on:click="flipCard">
		{{ face }}
	</div>
	
</template>


<script>

	export default {
		name: 'card',

		props: ['face', 'showing', 'index', 'flippable', 'flips'],

		data: function() {
			return {
			}
		},

		methods: {

			// uidLog: function() {
			// 	console.log('Unique ID: ', this._uid);
			// },

			flipCard: function() {
				if (this.flippable && this.flips < 2) {
					this.$emit('flipCard', this.index);
				}
			}
		}
	}
	
</script>


<style>

.card {
	border-radius: 8px;
	box-shadow: 2px 2px 8px #888;
	height: 150px;
	margin: 8px;
	transition: transform 1s;
  transform-style: preserve-3d;
  width: 150px;
}

.card:hover {
	box-shadow: 2px 2px 14px #888;
	cursor: pointer;
}

.back {
	background-color: #ccc;
	border: 10px solid white;
}

.front {
	background-color: #fff;
	border: 10px solid #ccc;
}
	
</style>