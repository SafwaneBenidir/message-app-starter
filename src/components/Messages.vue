<template>
  <div class="border">
    This is the messages
    <Message v-for="currentMessage in messages" :key="currentMessage.id" :message="currentMessage" v-on:message="updateLu"/>
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
    };
  },
  methods: {
    updateLu(message){
      message.read=true;
      this.message.read=true;
    }
  }
}
</script>

<style scoped>
.border {
  border-color: blue;
  border-width: 5px;
  border-style: solid;
  color: purple;
  font-size: 30px;
}
</style>