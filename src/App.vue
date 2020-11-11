<template>
  <div class="app">
    <HelloWorld :msg="'Welcome to Your Vue.JS App'"/>
    <Messages/>
    <Menu></Menu>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Messages from "./components/Messages.vue";
import Menu from "@/components/Menu";

export default {
  name: "App",
  components: {
    HelloWorld,
    Messages,
    Menu
  }
};
</script> 

<style>
html, body {
  height: 100%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
