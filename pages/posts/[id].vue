<script setup lang="ts">
  const { id } = useRoute().params
  const { data: posts } = useNuxtData('posts')
  const { data } = useLazyFetch(`https://jsonplaceholder.typicode.com/posts/${id}`, {
    key: `post-${id}`,
    default() {
      return posts.value.find((post: any) => post.id === id)
    }
  })
</script>

<template>
    <h3>{{ data['title'] }}</h3>
    <p>
      {{ data['body'] }}
    </p>
</template>
