<script setup lang="ts">
  defineProps<{
    color: string
    size: string
  }>()
</script>

<template>
  <button :class="`button button--${color} button--${size}`">
    Button
  </button>
</template>
