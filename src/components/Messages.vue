<template>
  <div class="border1">
    This is the messages
    <br />
    <br />
    <Message v-for="msg in messages" :key="msg.id" :message="msg.content" class="border2"/>
  </div>
</template>
<script>

import Message from "@/components/Message";
import {messagesMock} from "@/mocks/messages.mock";

export default {
  name: "Messages",
  components: {Message},
  data() {
    return {
      messages: messagesMock,
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.border1 {
  border:1px solid red;
}
.border2 {
  border:1px solid blue;
}
</style>
