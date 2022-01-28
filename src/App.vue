<template>
  <main class="sans-serif">
    <input v-model="message" />
    <box :text="message" shape="round" shader="gradient" :palette="0"/>
  </main>
</template>

<script setup>
import box from "./components/Box.vue";
import { ref } from 'vue';
  
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
const message = ref("Hello World");
  
</script>

<style>
</style>
