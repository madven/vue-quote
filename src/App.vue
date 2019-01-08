<template>
  <div class="container">
    <app-progress :count="quotes.length"></app-progress>
    <app-form @quote-added="addQuote"></app-form>
    <app-list @quote-clicked="deleteQuote" :quotes="quotes"></app-list>
    <div class="row">
      <div class="col-sm-12">
        <div class="alert alert-info text-center">Silmek icin tikla</div>
      </div>
    </div>
  </div>
</template>

<script>
import Progress from "./components/Progress.vue";
import Form from "./components/Form.vue";
import List from "./components/List.vue";

export default {
  data() {
    return {
      quotes: []
    };
  },
  methods: {
    addQuote(data) {
      if (this.quotes.length == 10) {
        alert("daha fazla olmaz");
      } else {
        this.quotes.push(data);
      }
    },
    deleteQuote(index) {
      new Audio(require("./assets/death.mp3")).play();
      this.quotes.splice(index, 1);
    }
  },
  components: {
    appProgress: Progress,
    appForm: Form,
    appList: List
  }
};
</script>

<style scoped>
</style>
