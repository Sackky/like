<template>
  <div id="app">
    <HelloWorld msg />
    <center>
      <h1>Vote for Members Black Pink</h1><br><br>
    </center>
    <div class="row">
      <div class="col-6">
        <center>
          <h2>Rosé (로제)</h2>
        </center>
        <img src="./assets/rose.jpg" width="50%" alt="pic 2" />
        <h4>Total {{total1}}</h4>
      </div>
      <div class="col-6">
        <center>
          <h2>Jennie (제니)</h2>
        </center>
        <img src="./assets/jennie.jpg" width="50%" alt="pic 2" />
        <h2>Total {{total2}}</h2>
      </div>
      <div class="col-6">
        <CsButton @cc="sum" />
      </div>
      <div class="col-6">
        <CsButton @cc="sum1" />
      </div>
      <br>
      <br>
      <div class="col-6">
        <center>
          <h2>Jisoo (지수)</h2>
        </center>
        <img src="./assets/jisoo.jpg" width="50%" alt="pic 2" />
        <h4>Total {{total1}}</h4>
      </div>
      <div class="col-6">
        <center>
          <h2>Lisa (리사)</h2>
        </center>
        <img src="./assets/lisa.jpg" width="60%" alt="pic 2" />
        <h4>Total {{total2}}</h4>
      </div>
      <div class="col-6">
        <CsButton @cc="sum" />
      </div>
      <div class="col-6">
        <CsButton @cc="sum1" />
      </div>
    </div>
  </div>
</template>
<script>
import HelloWorld from "./components/HelloWorld";
import CsButton from "./components/CsButton";

export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
  },
  data: function () {
    return {
      total1: 0,
      total2: 0,
    };
  },
  methods: {
    sum(counterValue) {
      this.total1 = counterValue;
    },

    sum1(counterValue) {
      this.total2 = counterValue;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: crimson;
  margin-top: 60px;
}
</style>