<template>
  <div class="row">
    <div class="col-sm-12">
      <h3>Quote Added</h3>
      <div class="progress" style="height: 20px;">
        <div
          class="progress-bar"
          role="progressbar"
          :style="{width:( quoteCount/maxQuotes ) * 100 + '%'}"
        >{{quoteCount}}/{{maxQuotes}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["quoteCount", "maxQuotes"]
};
</script>

<style>
</style>