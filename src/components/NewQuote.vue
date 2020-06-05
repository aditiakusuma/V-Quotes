<template>
  <div class="row">
    <form class="container center">
      <div class="form-group">
        <label>Quotes</label>
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
      </div>
      <div class="form-group">
        <!-- prevent mencegah agar click tidak mengirim request ke form submit -->
        <button class="btn btn-primary" @click.prevent="addQuote">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      quote: "isikan quote"
    };
  },
  methods: {
    addQuote() {
      // mengirim emit quote ke parent
      this.$emit("addedQuote", this.quote);
      //reset quote agar hilang
      this.quote = "";
    }
  }
};
</script>

<style>
</style>