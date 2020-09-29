<template>
    <div class="row">
        <form>
            <div class="col-sm-8 ">
                <label class="form-control">Quote</label>
                <textarea class="form-control" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 ">
               <button class="btn btn-primary" @click.prevent="createQuote">Add Quote</button>
            </div>
        </form>
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
            createQuote() {
                this.$emit('quoteCreated', this.quote);
                this.quote = '';
            }
        }
    };
</script>

<style>

</style>