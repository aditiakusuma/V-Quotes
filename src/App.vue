<template>
  <div class="container">
    <!-- addedQuote mengacu ke amit -->
    <new-quote-template @addedQuote="newQuote"></new-quote-template>
    <quoteGridTemplate :quotes="quotes"></quoteGridTemplate>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";

export default {
  data: function() {
    return {
      quotes: ["Quotes 1"],
      maxQuotes: 10
    };
  },
  components: {
    quoteGridTemplate: QuoteGrid,
    newQuoteTemplate: NewQuote
  },
  methods: {
    //parameter quote di ambil dari emit
    newQuote(quote) {
      // ambil variable quote dari parameter dan push ke data quotes
      this.quotes.push(quote);
    }
  }
};
</script>

<style>
</style>
