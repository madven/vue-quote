<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default quoteDiv">
      <div class="panel-body">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style scoped>
h4 {
  font-family: "Arizonia", cursive;
  font-size: 24px;
}
.quoteDiv {
  cursor: pointer;
}
.quoteDiv:hover {
  background-color: red;
}
</style>
