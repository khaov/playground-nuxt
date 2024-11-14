<script setup lang="ts">
  const items = [
    { title: "Быстрая выдача", text: "Вы получите деньги через 10 минут", image: "/images/item-1.png" },
    { title: "Надежность", text: "Все ваши данные защищены", image: "/images/item-2.png" },
  ];
</script>

<template>
  <h1>Frontend Projects</h1>
  <p>
    Project ideas to take you from beginner to advanced in Frontend
  </p>

  <div>
    <SharedCard
      v-for="(item, index) in items" :key="index"
      class=""
    >
    <span>
      {{ item.title }}
    </span>
  </SharedCard>
  </div>

</template>
