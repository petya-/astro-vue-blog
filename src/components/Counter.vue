<script setup>
import { ref } from 'vue'
const { initialCount } = defineProps({
  initialCount: {
    type: Number,
    default: 0,
    required: false,
  }
})
const counter = ref(initialCount)
</script>

<template>
  <button @click="$event => counter++">
    {{ counter }}
  </button>
  <slot></slot>
</template>