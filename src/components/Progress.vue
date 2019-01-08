<template>
  <div>
    <h2>Quotes Added</h2>
    <div class="progress">
      <div class="progress-bar" :style="{width: barWidth+'%'}">
        <span v-if="count > 0">{{count}}/10</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["count"],
  computed: {
    barWidth() {
      return this.count * 10;
    }
  }
};
</script>

<style>
</style>
