<template>
  <div id="app">
    <NavBar class="navbar"></NavBar>
	<HomePage class="homepage" msg="helloword"></HomePage>
  </div>
</template>

<script>
import HomePage from "./components/HomePage.vue";
import NavBar from "./components/NavBar.vue"
export default {
  name: "App",
  components: {
    NavBar,
    HomePage
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
}

html, body {
	width: 100%;
	height: 100%;
	margin: 0;
}

.navbar {
	width: 100%;
	height: 56px;
	background-color: #fff;
}
.homepage {
  width: 100%;
  height: 100%;
  background-color: beige;
}
</style>
