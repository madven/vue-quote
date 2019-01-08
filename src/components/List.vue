<template>
  <div class="row" style="margin: 30px auto">
    <app-quote v-for="(quote, index) in quotes" @click.native="quoteClick(index)">
      <h4>{{quote}}</h4>
    </app-quote>
  </div>
</template>

<script>
import Quote from "./Quote.vue";

export default {
  props: ["quotes"],
  components: {
    appQuote: Quote
  },
  methods: {
    quoteClick(index) {
      this.$emit("quote-clicked", index);
    }
  }
};
</script>

<style scoped>
</style>
