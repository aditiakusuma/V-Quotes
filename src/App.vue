<template>
  <div class="container">
    <progressBar :quoteCount="quotes.length" :maxQuotes="maxQuotes"></progressBar>
    <!-- addedQuote mengacu ke amit -->
    <new-quote-template @addedQuote="newQuote"></new-quote-template>
    <quoteGridTemplate :quotes="quotes" @quoteDeleted="deleteQuote"></quoteGridTemplate>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-danger" role="alert">Click on quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import Header from "./components/Header.vue";

export default {
  data: function() {
    return {
      quotes: ["Quotes 1"],
      maxQuotes: 10
    };
  },
  components: {
    quoteGridTemplate: QuoteGrid,
    newQuoteTemplate: NewQuote,
    progressBar: Header
  },
  methods: {
    //parameter quote di ambil dari emit
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("HEYY ITS FULL, DELETE ONE");
      }
      // ambil variable quote dari parameter dan push ke data quotes
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
