<template>
  <div class="col-sm-3">
    <div class="card text-center p-3">
      <div class="blockquote mb-0">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style>
.card {
  background-color: #ccc;
}

.card:hover {
  background-color: red;
}
</style>