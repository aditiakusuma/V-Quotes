<template>
  <div class="row">
    <quote-template v-for="quote in quotes">{{ quote }}</quote-template>
  </div>
</template>

<script>
import Quote from "./Quote.vue";

export default {
  props: ["quotes"],
  components: {
    quoteTemplate: Quote
  }
};
</script>

<style>
</style>