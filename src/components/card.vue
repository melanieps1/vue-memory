<template>

	<div class="card" v-bind:class="side" v-on:click="flipCard(side)"></div>
	
</template>


<script>

	export default {
		name: 'card',
		props: ['side'],
		methods: {
			flipCard: function(side) {
				// console.log(side);
				if (side === "back") {
					this.side = "front";
					// this.$emit('cardflipped', 'front');
				} else {
					this.side = "back";
				}
				// console.log(side);
			}
		}
	}
	
</script>


<style>

.card {
	border-radius: 10px;
	box-shadow: 2px 2px 8px #888;
	height: 200px;
	margin: 12px;
	transition: transform 1s;
  transform-style: preserve-3d;
  width: 200px;
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