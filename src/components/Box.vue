<template>
  <div :class="['box', shapeClass, colourClass]">{{ msg }}</div>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  text: String,
  shapeClass : String,
  shaderClass : String,
  colourClass : String
})

</script>