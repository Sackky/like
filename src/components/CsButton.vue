<template>
  <div>
    <button v-on:click="likeFunction" class="btn btn-primary ml-3">
      LIKE
      <svg
        width="1em"
        height="1em"
        viewBox="0 0 16 16"
        class="bi bi-chevron-compact-up"
        fill="currentColor"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          d="M7.776 5.553a.5.5 0 0 1 .448 0l6 3a.5.5 0 1 1-.448.894L8 6.56 2.224 9.447a.5.5 0 1 1-.448-.894l6-3z"
        />
      </svg>
      {{lable}}
    </button>
 &nbsp;
    <button v-on:click="wowFunction" class="btn btn-primary ml-3">
      WOW
      <svg
        width="1em"
        height="1em"
        viewBox="0 0 16 16"
        class="bi bi-chevron-double-up"
        fill="currentColor"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          d="M7.646 2.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1-.708.708L8 3.707 2.354 9.354a.5.5 0 1 1-.708-.708l6-6z"
        />
      </svg>
      {{lable}}
    </button>
    <button v-on:click="LoveFunction" class="btn btn-primary ml-3">
      LOVE
      <svg
        width="1em"
        height="1em"
        viewBox="0 0 16 16"
        class="bi bi-heart"
        fill="currentColor"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          d="M8 2.748l-.717-.737C5.6.281 2.514.878 1.4 3.053c-.523 1.023-.641 2.5.314 4.385.92 1.815 2.834 3.989 6.286 6.357 3.452-2.368 5.365-4.542 6.286-6.357.955-1.886.838-3.362.314-4.385C13.486.878 10.4.28 8.717 2.01L8 2.748zM8 15C-7.333 4.868 3.279-3.04 7.824 1.143c.06.055.119.112.176.171a3.12 3.12 0 0 1 .176-.17C12.72-3.042 23.333 4.867 8 15z"
        />
      </svg>
      {{lable}}
    </button>
    <button v-on:click="unlikeFunction" class="btn btn-primary ml-3">
      UNLIKE
      <svg
        width="1em"
        height="1em"
        viewBox="0 0 16 16"
        class="bi bi-chevron-double-down"
        fill="currentColor"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          d="M1.646 6.646a.5.5 0 0 1 .708 0L8 12.293l5.646-5.647a.5.5 0 0 1 .708.708l-6 6a.5.5 0 0 1-.708 0l-6-6a.5.5 0 0 1 0-.708z"
        />
      </svg>
      {{lable}}
    </button>
    <button v-on:click="ResetFunction" class="btn btn-info ml-3">
      RESET SUM
      <svg
        width="1em"
        height="1em"
        viewBox="0 0 16 16"
        class="bi bi-arrow-counterclockwise"
        fill="currentColor"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          d="M12.83 6.706a5 5 0 0 0-7.103-3.16.5.5 0 1 1-.454-.892A6 6 0 1 1 2.545 5.5a.5.5 0 1 1 .91.417 5 5 0 1 0 9.375.789z"
        />
      </svg>
      {{lable}}
    </button>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    likeFunction: function () {
      this.counter += 1;
      this.$emit("cc", this.counter);
    },
    wowFunction: function () {
      this.counter += 1;
      this.$emit("cc", this.counter);
    },
    LoveFunction: function () {
      this.counter += 1;
      this.$emit("cc", this.counter);
    },
    unlikeFunction: function () {
      this.counter += -1;
      this.$emit("cc", this.counter);
    },
    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>