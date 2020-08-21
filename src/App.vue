<template>
  <div id="app">
    <HelloWorld msg="press a button" />
    <hr />
    <div class="row">
      <div class="col-6">
        <img alt="Vue logo" src=".\assets\img\1.jpg" width="350" />
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
        <img alt="Vue logo" src=".\assets\img\2.jpg" width="300px" />
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CSButton @cc="sum" />
      </div>
      <div class="col-6">
        <CSButton @cc="sum1" />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import CSButton from "./components/csbutton";

export default {
  name: "App",
  components: {
    HelloWorld,
    CSButton,
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
body {
 background-image: url("./assets/img/sky.jpg");
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffe600;
  margin-top: 100px;
  margin-right: 100px;
}
</style>
