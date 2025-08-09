<script setup lang="ts">
const route = useRoute();
const selTitle = route.query?.title;

const { data: post } = (await useAsyncData("products", () =>
  queryCollection("products")
    .path(selTitle as string)
    .first()
)) as Record<string, any>;
</script>

<template>
  <div>
    <h1>Blog</h1>
    <h2>{{ post?.title }}</h2>
    <h2>{{ post?.meta.price }}</h2>
    <br />
    <ContentRenderer :value="post" />
  </div>
</template>
