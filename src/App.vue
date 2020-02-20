<template>
    <div class="container">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue'
    import NewQuote from './components/NewQuote.vue'

    export default {
        data: function () {
            return {
                quotes: [
                    'A single Quote',
                    'A single Quote 2',
                    'A single Quote 3',
                ],
                maxQuotes: 10
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: NewQuote
        },
        methods: {
            newQuote(quote) {
                this.quotes.push(quote);
            }
        },
    }
</script>

<style>
</style>
