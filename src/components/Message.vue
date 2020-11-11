<template>
  <div class="border1">
    <img v-bind:src="message.sender.profileImage"/>

    <span class="name">{{ message.sender.name }}</span>
    <div class="checkbox">
      <input type="checkbox" id="checkbox" v-model="checked">
      <label for="checkbox">{{ checked }}</label>
    </div>
    <br>
    <span class="content">{{ message.content }}</span>
  </div>
</template>

<script>
export default {
  name: "Message",
  data() {
    return {
      checked: false
    }
  },
  props: {
    message: Object,
  }
}
</script>

<style scoped>
.border1 {
  position: relative;
  margin-left: auto;
  margin-right: auto;
  height: 100px;
  width: 500px;
  border-color: cornflowerblue;
  border-width: 1px;
  border-style: solid;
  overflow:hidden;
}

img {
  float: left;
  width: 100px;
  height: 100px;
  border-radius: 50%;
}

.checkbox {
  float: right;
  margin: auto;
  width: 1%;
  border: 3px solid green;
  padding: 30px;
  color: black;
  font-size: 10px;
}

.name {
  float: left;
  margin-left: 15px;
  color: black;
  font-size: 30px;
}

.content {
  margin-left: 10px;
  color: blue;
  font-size: 15px;
}
</style>