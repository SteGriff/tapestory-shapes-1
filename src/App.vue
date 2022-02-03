<template>
  <main class="sans-serif w-99 measure center mv4">
<!--     <input v-model="message" /> -->
    
    <box :text="message" shape="round" shader="g135" :palette="palette"/>
    <div class="mv4 ba br4 overflow-hidden">
      <div class="overflow-x-scroll pv3 ph2 ws-nw">
        <div v-for="p in palettes" :class="['palette' + p]" class="mh1 dib ba pal br2 pointer overflow-hidden">
          <div class="dib palSlice bg-first"></div>
          <div class="dib palSlice bg-second"></div>
          <div class="dib palSlice bg-third"></div>
          <div class="dib palSlice bg-fourth"></div>
          <div class="dib palSlice bg-fifth"></div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
import box from "./components/Box.vue";
import { ref } from 'vue';
  
const message = ref("Hello World");
const palettes = [0,1,3,5,6,7,8,11,12,13,14,15,16,17,18,20,22,23,26,27,28,29,34,35,37,38,40,45,47,50,55,57,60,67,69,71,73];
const shaders = ['1', 'g135', 'g12345', 'a','b','c','d','e']
  
const palette = ref(0);

</script>

<style>
</style>
