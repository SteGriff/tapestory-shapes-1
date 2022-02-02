<template>
  <main class="sans-serif w-99 measure center mv4">
<!--     <input v-model="message" /> -->
    
    <box :text="message" shape="round" shader="gradient" :palette="0"/>
    <div class="mv4 ba br4">
      <div class="overflow-x-scroll pa3">
        <div v-for="p in palettes" :class="['palette' + p, 'mh1', 'dib']">
          <div class="dib w1 h2 bg-first"></div>
          <div class="dib w1 h2 bg-second"></div>
          <div class="dib w1 h2 bg-third"></div>
          <div class="dib w1 h2 bg-fourth"></div>
          <div class="dib w1 h2 bg-fifth"></div>
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
const palettes = [0,1,3,5,6,7,8,11,12,13,14,15,16,17,18,20,22,23,26,27,28,29,34,35,37,38,40,45,47,50,55,57,60,67,69,71,73];

</script>

<style>
</style>
