<template>

	<div class="card" v-bind:class="{ 'back': showing == 'back' }" v-on:click="flipCard"> {{ face }} </div>
	
</template>


<script>

	export default {
		name: 'card',

		props: ['face', 'showing'],

		data: function() {
			return {
				// cardId: this._uid
			}
		},

		methods: {

			uidLog: function() {
				console.log('Unique ID: ', this._uid);
			},

			flipCard: function() {
				this.$emit('flipCard');
				alert('card flipped');
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