<template>
    <div class="container">
        <quote-grid :quotes="quotes"></quote-grid>
    </div>
</template>

<script>

import QuoteGrid from './components/QuoteGrid.vue'
    export default {
        data: function(){
            return {
                quotes: ['Placeholder quote'],
                maxQuotes: 10
            }
        },
        components: {
            quoteGrid: QuoteGrid
        }
        
    }
</script>

<style>
</style>
