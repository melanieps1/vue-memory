<template>
	
	<div class="board">
		<table>
			<tbody>
				<tr>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
				</tr>
				<tr>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
				</tr>
				<tr>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
				</tr>
				<tr>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
					<td><card side="back" /></td>
				</tr>
			</tbody>
		</table>
	</div>

</template>


<script>

import card from './card.vue'

export default {
	name: 'board',
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