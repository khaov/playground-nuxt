<script setup lang="ts">
  const { data: posts } = useNuxtData('posts')
</script>

<template>
  <ul>
    <li v-for="post in posts">
      <UCard>
        <NuxtLink :to="`/posts/${post['id']}`">
          <h3>{{ post['title'] }}</h3>
          <p>
            {{ post['body'] }}
          </p>
        </NuxtLink>
      </UCard>
    </li>
  </ul>
</template>