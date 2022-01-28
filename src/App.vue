<template>
  <main>
    <h1>{{message}}</h1>
    <input v-model="message">
    <Box 
  </main>
</template>

<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import { ref } from 'vue';
  
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
const message = ref("Hello World");
  
</script>

<style>
</style>
