<template>
  <div contenteditable
       class="box tc b"
       :class="['shape' + shape, 'shader' + shader, 'palette' + palette, foreground]"
       >
    {{ text }}
  </div>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  text: String,
  shape : String,
  shader : String,
  palette : Number,
  foreground: String
})

</script>