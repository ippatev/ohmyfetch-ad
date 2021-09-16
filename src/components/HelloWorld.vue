<template>
  <img alt="Vue logo" :src="props.url" />
  <div>{{ props.msg }}</div>
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps({
  msg: String,
  url: String,
});
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
