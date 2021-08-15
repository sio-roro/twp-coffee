<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  width: 100%;
  color: rgba(120, 120, 120, 1);
  font-family: serif;
  scroll-behavior: smooth;
}
</style>
