<template lang="html">

	<div class="textarea">
		<textarea :id="id" :rows="row" :cols="column" class="form" :name="name" @input="changeHandling" @change="changeHandling" />
	</div>

</template>

<script lang="js">

	export default {
		name: 'customTextarea',
		props: {
			id: String,
			name: String,
			row: String,
			column: String
		},
		mounted () {

		},
		data () {
			return {

			}
		},
		methods: {
			changeHandling ({ type, target }) {
			const event = {
				type,
				isCheckbox: target.type === 'checkbox',
				target: {
					value: target.value,
					checked: target.checked
				}
			}
			console.log(`${event.type}: ${event.isCheckbox ? event.target.checked : event.target.value}`);
			}
		},
		computed: {

		}
}


</script>

<style scoped lang="scss">
	.textarea {

	}
</style>
