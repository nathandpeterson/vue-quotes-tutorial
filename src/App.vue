<template>
    <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <quote-grid :quotes="quotes"
                    @removeQuote="removeQuote"
        ></quote-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">
                    Info: Click on a Quote to delete it!
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Header from './components/Header.vue'
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'
    export default {
        data: function(){
            return {
                quotes: ['Placeholder quote'],
                maxQuotes: 10
            }
        },
        components: {
            quoteGrid: QuoteGrid,
            appNewQuote: NewQuote,
            appHeader: Header
        },
        methods: {
            newQuote(quote){
                if(this.quotes.length >= 10) return alert('You have reached the maximum number of quotes. Delete a quote to add more.')
                this.quotes.push(quote)
            },
            removeQuote(index){
                this.quotes.splice(index, 1)
            }
        },
        
    }
</script>

<style>
</style>
