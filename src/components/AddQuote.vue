<template>
    <div >
        <section id="cover" class="min-vh-100">
            <div id="cover-caption">
                <div class="container">
                    <div class="row text-white">
                        <div class="col-xl-5 col-lg-6 col-md-8 col-sm-10 mx-auto text-center form">
                            <h4 class="display-5  py-2 ">Write your quote here</h4>
                            <div class="px-2">
                                <form action="" class="justify-content-center">
                                    <div class="form-group">
                                        <label class="sr-only">Write your quotes</label>
                                        <textarea class="form-control" v-model="quote"  required pattern="[0-9a-zA-Z_.-]*"></textarea>
                                    </div>
                                    
                                    <button class="btn btn-success btn-lg mb-3" @click.prevent="addQuote" >Add Quote</button>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            };
        },
        methods: {
            addQuote() {
                this.$emit('quoteCreated', this.quote);
                this.quote = '';
            }
        }
    };
</script>

<style >
    #cover {
    background: #222 url('../img/cover.jpg') center center no-repeat;
    background-size: cover;
    height: 100%;
    text-align: center;
    display: flex;
    align-items: center;
    position: relative;
}

#cover-caption {
    width: 100%;
    position: relative;
    z-index: 1;
}

/* only used for background overlay not needed for centering */
form:before {
    content: '';
    height: 100%;
    left: 0;
    position: absolute;
    top: 0;
    width: 100%;
    background-color: rgba(0,0,0,0.3);
    z-index: -1;
    border-radius: 10px;
}
</style>