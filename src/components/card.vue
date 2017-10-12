<template>

	<div class="card" v-bind:class="cardId" v-on:click="helpMe"></div>
	
</template>


<script>

	export default {
		name: 'card',
		props: ['side'],
		data() {
			return {
				cardId: this._uid
			}
		},
		methods: {

			helpMe() {
				console.log(this._uid);
			}

			// flipCard: function(side) {
			// 	// console.log(side);
			// 	if (side === "back") {
			// 		this.side = "front";
			// 		// this.$emit('cardflipped', 'front');
			// 	} else {
			// 		this.side = "back";
			// 	}
			// 	// console.log(side);
			// }
		}
	}
	
</script>


<style>

.card {
	border-radius: 10px;
	box-shadow: 2px 2px 8px #888;
	height: 125px;
	margin: 8px;
	transition: transform 1s;
  transform-style: preserve-3d;
  width: 125px;
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
	border: 10px solid #222;
}
	
</style>