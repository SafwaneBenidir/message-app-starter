<template>
  <div class="border">
    This is the menu
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
.border{
  margin-left: auto;
  margin-right: auto;
  border-color: yellow;
  border-width: 5px;
  border-style:solid;
  color: purple;
  font-size: 30px;
}
</style>