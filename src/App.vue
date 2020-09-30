<template>
    <div >
        <app-header></app-header>
        <hr>
        <div >
            <app-add-quote @quoteCreated="appendQuote"></app-add-quote>
        </div>
        
        <div>
            <app-quote-array :quotes="quotes" ></app-quote-array>
        </div>

        <div>
            <app-footer></app-footer>
        </div>
    	
    </div>
</template>

<script>
    import Header from './components/shared/Header.vue'
    import Footer from './components/shared/Footer.vue'
    import AddQuote from './components/AddQuote.vue'
	import QuotesArray from './components/QuotesArray.vue'
    export default {

        data (){
        	return {
                q:'',
        		quotes : [
        			'WonderFul Quotes'
        		],
        		max : 10
        	}
        },
        methods : {
            appendQuote($emit){
                this.quotes.push($emit);

            }
        },

        components : {
        	appQuoteArray : QuotesArray,
            appAddQuote : AddQuote,
            appHeader : Header,
            appFooter : Footer
        }
    };
</script>

<style>
</style>
