<script setup lang="ts">
  const { data: posts } = useNuxtData('posts')
</script>

<template>
  <h1>Последние посты</h1>
  <ul v-if="posts">
    <li v-for="post in posts.slice(0, 4)" :key="post.id">
      <Card
        :id=post.id
        :title=post.title
        :body=post.body
      />
    </li>
  </ul>
  <p v-else>Ошибка закгрузки данных</p>
</template>
