<template>
  <div class="row">
    <div class="col">
      <div>
        <button @click="wowFunction()" class="btn btn-info">
          <i class="fa fa-thumbs-o-up" aria-hidden="true"></i>
        </button>
        <button @click="likeFunction()" class="btn btn-info">
          <i class="fa fa-thumbs-o-up" aria-hidden="true"></i>
        </button>
        <button @click="unlikeFunction()" class="btn btn-info">
          <i class="fa fa-thumbs-o-down" aria-hidden="true"></i>
        </button>
        <button @click="miniheart()" class="btn btn-info">
          <i class="fa fa-heart-o" aria-hidden="true"></i>
        </button>
        <button @click="resetFunction()" class="btn btn-info">
          <i class="fa fa-retweet" aria-hidden="true"></i>
        </button>
        <p v-bind:style="{fontSize: fsize + 'px'}">{{counter}}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "CsBotton",
  data: function () {
    return {
      counter: 0,
      fsize: 25,
    };
  },
  props: {
    label: String,
  },
  methods: {
    wowFunction: function () {
      this.counter += 1;
      this.$emit("", this.counter);
      console.log(this.counter);
    },
    likeFunction: function () {
      this.counter += 1;
      this.$emit("", this.counter);
      console.log(this.counter);
    },
    unlikeFunction: function () {
      this.counter -= 1;
      console.log(this.counter);
    },
    miniheart: function () {
      this.counter += 5;
      console.log(this.counter);
    },
    resetFunction: function () {
      this.counter = 0;
      console.log(this.counter);
    },
  },
};
</script>
<style>
</style>