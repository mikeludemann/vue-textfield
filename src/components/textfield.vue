<template lang="html">

	<div class="textfield--custom">
		<input type="text" class="form" v-bind:name="name" @input="changeHandling" @change="changeHandling" />
	</div>

</template>

<script lang="js">

	export default {
		name: 'textfield',
		props: {
			name: String
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
	.textfield--custom {

	}
</style>
