<script setup lang="ts">
    const { data } = await useFetch('https://jsonplaceholder.typicode.com/posts', {key: 'posts'})
</script>

<template>
    <AppHeader />
    <main>
        <slot />
    </main>
    <AppFooter />
</template>