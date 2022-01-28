<template>
  <div :class="['box', 'shape' + shape, 'shader' + shader, 'palette' + palette]">{{ text }}</div>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  text: String,
  shape : String,
  shader : String,
  palette : String
})

</script>