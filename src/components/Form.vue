<template>
  <div class="row">
    <div class="col-sm-6 col-sm-offset-3">
      <form>
        <label for="comment">Quote:</label>
        <textarea
          class="form-control"
          rows="3"
          id="comment"
          v-model="quote"
          @keyup.enter="addQuote"
        ></textarea>
        <div style="margin: 10px auto; text-align: center;">
          <button type="button" class="btn btn-primary" @click.prevent="addQuote">Add Quote</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quote: ""
    };
  },
  methods: {
    addQuote() {
      if (this.quote) {
        new Audio(require("./../assets/wololoo.mp3")).play();
        this.$emit("quote-added", this.quote);
        this.quote = "";
      }
    }
  }
};
</script>

<style>
</style>
