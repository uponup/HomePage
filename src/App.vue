<template>
  <div id="app">
    <vHeader>
      <HomePage class="homepage" msg="helloword"></HomePage>
    </vHeader>
  </div>
</template>

<script>
import vHeader from "./components/Header.vue";
import HomePage from "./components/HomePage.vue";

export default {
  name: "App",
  components: {
    vHeader,
    HomePage
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.homepage {
  width: 100%;
  height: 100%;
  background-color: beige;
}
</style>
