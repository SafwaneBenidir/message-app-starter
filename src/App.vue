<template>
  <div class="app">
    <HelloWorld v-on:event-key="doSomething" :msg="'Welcome to Your Vue.JS App'"/>
    <Messages/>
    <Menu></Menu>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Messages from "./components/Messages.vue";
import Menu from "@/components/Menu";

/*import moment from 'moment';
import Vue from 'vue';

Vue.filter('formatDate', function(value) {
  if (value) {
    return moment(String(value)).format('MM/DD/YYYY hh:mm')
  }
});*/

export default {
  name: "App",
  components: {
    HelloWorld,
    Messages,
    Menu
  },
  methods: {
    doSomething(message){
      alert(message);
    }
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
