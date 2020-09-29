<template>
    <div class="container">
    	<app-quote-array :quotes="quotes"></app-quote-array>
    </div>
</template>

<script>
	import QuotesArray from './components/QuotesArray.vue'
    export default {

        data (){
        	return {
        		quotes : [
        			'WonderFul Quotes',
        			'Holla Game over'
        		],
        		max : 10
        	}
        },

        components : {
        	appQuoteArray : QuotesArray
        }
    };
</script>

<style>
</style>
