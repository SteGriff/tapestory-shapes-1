<template>
  <div class="ph2">
    <main class="sans-serif w-99 measure center mv4">
      <!--     <input v-model="message" /> -->

      <box
        :text="message"
        shape="round"
        :shader="shader"
        :palette="palette"
        :foreground="foreground"
      />

      <!-- Palette Selector -->
      <div class="mv4 ba br4 overflow-hidden">
        <div class="overflow-x-auto pv3 ph2 ws-nw">
          <div
            v-for="p in palettes"
            :class="['palette' + p]"
            class="mh1 dib ba sqr32 br2 pointer overflow-hidden"
            @click="setPalette(p)"
          >
            <div class="dib palSlice bg-first"></div>
            <div class="dib palSlice bg-second"></div>
            <div class="dib palSlice bg-third"></div>
            <div class="dib palSlice bg-fourth"></div>
            <div class="dib palSlice bg-fifth"></div>
          </div>
        </div>
      </div>

      <!-- Shader Selector -->
      <div class="mv4 ba br4 overflow-hidden">
        <div class="overflow-x-auto pv3 ph2 ws-nw">
          <div
            v-for="s in shaders"
            :class="['shader' + s, 'palette' + palette]"
            class="mh1 dib sqr32 br2 pointer"
            @click="setShader(s)"
          ></div>
        </div>
      </div>

      <!-- Forground Selector -->
      <div class="mv4 ba br4 overflow-hidden">
        <div class="overflow-x-auto pv3 ph2 ws-nw">
          <div
            v-for="f in foregrounds"
            :class="['shader' + shader, 'palette' + palette, f]"
            class="mh1 dib pa1 b br2 pointer"
            @click="setForeground(f)"
          >
            {{ f }}
          </div>
        </div>
      </div>

      <!-- Debug -->
      <ul>
        <li>Palette {{ palette }}</li>
        <li>Shader {{ shader }}</li>
        <li>Foreground {{ foreground }}</li>
      </ul>
    </main>
  </div>
</template>

<script setup>
import box from "./components/Box.vue";
import { ref } from "vue";

const message = ref("Hello World");

// Ya I know it's not very "compositional" rn

// Options
  // TODO Import from TS files?
const palettes = [
  0, 1, 3, 5, 6, 7, 8, 11, 12, 13, 14, 15, 16, 17, 18, 20, 22, 23, 26, 27, 28,
  29, 34, 35, 37, 38, 40, 45, 47, 50, 55, 57, 60, 67, 69, 71, 73,
];
const shaders = [
  "1",
  "2",
  "3",
  "4",
  "5",
  "g13",
  "g35",
  "g135",
  "a",
  "b"
];
const foregrounds = [
  "black",
  "white",
  "first",
  "second",
  "third",
  "fourth",
  "fifth",
];

// Selection
const palette = ref(0);
const shader = ref("g135");
const foreground = ref("white");

// Functions
const setPalette = (p) => {
  palette.value = p;
};

const setShader = (s) => {
  shader.value = s;
};

const setForeground = (c) => {
  foreground.value = c;
};
</script>

<style></style>
