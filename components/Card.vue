
<!-- <script setup lang="ts">
  defineProps<{
    id: string
    title: string
    body: string
  }>()
</script> -->

<script setup>
  defineProps({
    id: { type: Number, required: true },
    title: { type: String, required: true},
    body: { type: String, required: true }
  })
</script>

<template>
  <NuxtLink :to="`/posts/${id}`">
    <h3>{{ title }}</h3>
    <p>{{ body }}</p>
  </NuxtLink>
</template>
