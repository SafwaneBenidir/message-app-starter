<template>
  <div class="hello">
    <h1>{{msg}}</h1>
    <button v-on:click="say('salut')">Dire salut</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  methods: {
    say(message){
      this.$emit("event-key",message);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 40px 0 0;
}
</style>
