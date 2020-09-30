<template>
    <div class="container.fluid">
        <app-header></app-header>
        <hr>
        <app-add-quote></app-add-quote>
        <div>
            <app-quote-array :quotes="quotes"></app-quote-array>
        </div>
    	
    </div>
</template>

<script>
import Header from './components/Header.vue'
    import AddQuote from './components/AddQuote.vue'
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
        	appQuoteArray : QuotesArray,
            appAddQuote : AddQuote,
            appHeader : Header
        }
    };
</script>

<style>
</style>
