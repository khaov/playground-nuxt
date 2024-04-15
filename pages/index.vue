<script setup lang="ts">
  const { data: posts } = useNuxtData('posts')
</script>

<template>
  <h1>Последние посты</h1>
  <ul v-if="posts">
    <li v-for="post in posts.slice(0, 4)">
      <UCard>
        <NuxtLink :to="`/posts/${post.id}`">
          <h3>{{ post.title }}</h3>
          <p>
            {{ post.body }}
          </p>
        </NuxtLink>
      </UCard>
    </li>
  </ul>
  <p v-else>Ошибка закгрузки данных</p>
</template>
