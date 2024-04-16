<script setup lang="ts">

  await useFetch(
    'https://jsonplaceholder.typicode.com/posts', {key: 'posts'}
  )

  // await useAsyncData(
  //   'posts', () => $fetch('https://jsonplaceholder.typicode.com/posts')
  // )

</script>

<template>
    <AppHeader />
    <main>
        <slot />
    </main>
    <AppFooter />
</template>
