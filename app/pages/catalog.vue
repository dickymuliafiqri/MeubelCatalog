<script setup lang="ts">
const { data: posts } = await useAsyncData("products", () => queryCollection("products").all());
</script>

<template>
  <div>
    <h1>Blog</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        <NuxtLink :to="'/product?title=' + post.path">{{ post.title }}</NuxtLink>
      </li>
    </ul>
  </div>
</template>
