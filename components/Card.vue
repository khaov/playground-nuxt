
<script setup lang="ts">
  defineProps<{
    id?: string
    title?: string
    body?: string
  }>()
</script>

<template>
  <NuxtLink :to="`/posts/${id}`">
    <h3>{{ title }}</h3>
    <p>{{ body }}</p>
  </NuxtLink>
</template>
