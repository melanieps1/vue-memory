<template>
	
	<div class="board">
		<table>
			<tbody>
				<tr
					is="card"
					v-for"card in cards"></tr>

				<!-- <tr>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
				</tr>
				<tr>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
				</tr>
				<tr>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
				</tr>
				<tr>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
					<td><card /></td>
				</tr> -->
			</tbody>
		</table>
	</div>

</template>


<script>

import card from './card.vue'

export default {
	name: 'board',

	data: 
		deck: {
			cards: [
				
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
		},

	components: {
		card
	},

	methods: {



	}
	
}
	
</script>


<style>

	table {
		margin: auto;
	}
	
</style>