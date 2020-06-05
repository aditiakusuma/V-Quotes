<template>
  <div class="row">
    <!-- native digunakan untuk click pada element tersebut, ambil index array kemudian pass ke fungsi nya -->
    <quote-template v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</quote-template>
  </div>
</template>

<script>
import Quote from "./Quote.vue";

export default {
  props: ["quotes"],
  components: {
    quoteTemplate: Quote
  },
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  }
};
</script>

<style>
</style>