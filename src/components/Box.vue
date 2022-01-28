<template>
  <div :class="['box', shapeClass, colourClass]">{{ msg }}</div>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  text: String,
  shape : String,
  shader : String,
  colour : String
})

</script>