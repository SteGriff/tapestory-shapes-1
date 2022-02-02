<template>
  <main class="sans-serif w-99 measure center mv4">
<!--     <input v-model="message" /> -->
    
    <box :text="message" shape="round" shader="gradient" :palette="0"/>
    <div class="mv4 ba br4">
      <div class="overflow-x-scroll pa4">
        <div v-for="p of palettes" :class="'palette' + p">
        </div>
      </div>
    </div>
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
