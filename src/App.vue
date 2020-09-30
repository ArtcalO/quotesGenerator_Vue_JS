<template>
    <div >
        <app-header :quotes="quotes" :max="max"></app-header>
        <hr>
        <div >
            <app-add-quote @quoteCreated="appendQuote"></app-add-quote>
        </div>
        
        <div class="m-2 p-2" >
            <app-quote-array :quotes="quotes"  @selecteQuoteIndex="spliceQuote" ></app-quote-array>
        </div>
        <div class=" col-sm alert alert-primary mx-auto text-center" role="alert">
              Tip : Click on a quote to delete it !
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
        		quotes : [
        			'WonderFul Quotes'
        		],
        		max : 10
        	}
        },
        methods : {
            
            appendQuote($emit){
                var disallowed = $emit.match(/^\s+$/);
                if(disallowed == null && $emit != "" ){
                    if(this.quotes.length < this.max){

                        this.quotes.push($emit);
                    }
                    else{
                        alert("Quotes are full, please delete some to add others !")
                    }
                }
                else{
                    alert("Input a valid Quote \n No blank space allowed as quote");
                }
                

            },
            spliceQuote($emit){ 

                this.quotes.splice($emit, 1);

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
