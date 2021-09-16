<template>
  <suspense>
    <template #default>
      <HelloWorld :msg="todo?.title" :url="todo?.url" />
    </template>
    <template #fallback>
      <span>Loading ...</span>
    </template>
  </suspense>
</template>

<script setup>
import { ref } from "vue";
import { $fetch } from "ohmyfetch";
import HelloWorld from "./components/HelloWorld.vue";

let todo = ref({});
todo.value = await $fetch("https://jsonplaceholder.typicode.com/photos/1");
</script>
<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
