<script setup lang="ts">

  // const { data } = await useFetch(
  //   'https://jsonplaceholder.typicode.com/posts', {key: 'posts'}
  // )

  const {} = await useAsyncData(
    'posts', () => $fetch('https://jsonplaceholder.typicode.com/posts')
  )

</script>

<template>
    <AppHeader />
    <main>
        <slot />
    </main>
    <AppFooter />
</template>
