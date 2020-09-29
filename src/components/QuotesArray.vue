<template>
	<div class="row">
		<app-add-quote></app-add-quote>
		<app-quote v-for="quote in quotes">{{ quote }}</app-quote>
	</div>
</template>

<script>
	import AddQuote from './AddQuote.vue'
	import Quote from './Quotes.vue'
	export default {
		props : ['quotes'],
		components : {
			appQuote : Quote,
			appAddQuote : AddQuote
		}
	};
</script>

<style >
	

</style>