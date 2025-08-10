<script setup lang="ts">
const { data: posts } = await useAsyncData("products", () => queryCollection("products").all());
</script>

<template>
  <UContainer class="py-10">
    <h1 class="text-3xl font-bold mb-6 text-center">Katalog Produk</h1>

    <UGrid :columns="[1, 2, 4]" gap="6">
      <NuxtLink v-for="post in posts" :key="post.id" :to="`/product?title=${post.path}`" target="_blank">
        <UCard class="cursor-pointer hover:shadow-lg transition">
          <!-- Gambar produk -->
          <img :src="post.meta.image as string" :alt="post.title" class="w-full h-48 object-cover rounded" />

          <!-- Info produk -->
          <div class="p-4">
            <h3 class="font-bold mb-2">{{ post.title }}</h3>
            <p class="text-primary font-semibold">{{ post.meta.price }}</p>
          </div>
        </UCard>
      </NuxtLink>
    </UGrid>
  </UContainer>
</template>

<style scoped>
.text-primary {
  color: #1e88e5;
}
</style>
