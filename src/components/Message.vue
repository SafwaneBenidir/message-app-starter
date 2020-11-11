<template>
    <div class="border1">
      <img v-bind:src="message.sender.profileImage" class="img"/>
      <span class="name">{{message.sender.name}}</span>
      <br>
      <span class="content">{{message.content}}</span>
    </div>
</template>

<script>
export default {
    name: "Message",
    props: {
        message: Object,
        }
}
</script>

<style scoped>
.border1{
  position: relative;
  margin-left: auto;
  margin-right: auto;
  width: 500px;
  border-color: cornflowerblue;
  border-width: 1px;
  border-style:solid;
}

.img {
  float:left;
  width: 100px;
  height: 100px;
  border-radius: 50%;
}

.name{
  float:left;
  margin-left: 15px;
  color: black;
  font-size: 30px;
}

.content{
  margin-left: 10px;
  color: blue;
  font-size: 15px;
}
</style>