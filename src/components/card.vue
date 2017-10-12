var cards = [
	
	{
		name: 'circle',
		image: '../assets/images/circle.png',
		id: 1
	},
	{
		name: 'diamond',
		image: '../assets/images/diamond.png',
		id: 2
	},
	{
		name: 'heart',
		image: '../assets/images/heart.png',
		id: 3
	},
	{
		name: 'oval',
		image: '../assets/images/oval.png',
		id: 4
	},
	{
		name: 'pentagon',
		image: '../assets/images/pentagon.png',
		id: 5
	},
	{
		name: 'rectangle',
		image: '../assets/images/rectangle.png',
		id: 6
	},
	{
		name: 'square',
		image: '../assets/images/square.png',
		id: 7
	},
	{
		name: 'star',
		image: '../assets/images/star.png',
		id: 8
	},
	{
		name: 'triangle',
		image: '../assets/images/triangle.png',
		id: 9
	},
	{
		name: 'x',
		image: '../assets/images/x.png',
		id: 10
	}

];

<template>

	<div class="card" v-bind:class="cardId" v-on:click="uidLog"></div>
	
</template>


<script>

	export default {
		name: 'card',

		props: ['cards', 'image'],

		data() {
			return {
				cardId: this._uid
			}
		},

		methods: {

			uidLog() {
				console.log('Unique ID: ', this._uid);
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
/*  background-color: #ccc;
	border: 10px solid white;*/
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