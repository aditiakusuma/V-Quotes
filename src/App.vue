<template>
  <div class="container">
    <quotesGridTemplate :quotes="quotes"></quotesGridTemplate>
  </div>
</template>

<script>
import QuotesGrid from "./components/QuoteGrid.vue";

export default {
  data: function() {
    return {
      quotes: ["Quotes 1"],
      maxQuotes: 10
    };
  },
  components: {
    quotesGridTemplate: QuotesGrid
  }
};
</script>

<style>
</style>
