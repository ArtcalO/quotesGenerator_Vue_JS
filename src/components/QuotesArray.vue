<template>
	<div class="row">
		<app-quote v-for="(quote, i) in quotes" @click.native="getQuoteIndex(i)">{{ quote }}</app-quote>
	</div>
</template>

<script>
	import Quote from './Quotes.vue'
	export default {
		props : ['quotes'],
		components : {
			appQuote : Quote
		},
		methods : {
			getQuoteIndex (i){
				this.$emit('selecteQuoteIndex', i);
			}
		}
	};
</script>

<style >
	

</style>