<script setup lang="ts">
const route = useRoute();
const selTitle = route.query?.title;

// Ambil data produk berdasarkan path
const { data: post } = (await useAsyncData("products", () =>
  queryCollection("products")
    .path(selTitle as string)
    .first()
)) as Record<string, any>;

function goToWhatsApp() {
  const phone = "628123456789"; // ganti dengan nomor WA pemilik
  const message = `Halo, saya ingin memesan produk: ${post?.title}`;
  window.open(`https://wa.me/${phone}?text=${encodeURIComponent(message)}`, "_blank");
}
</script>

<template>
  <UContainer class="py-10">
    <UCard v-if="post" class="max-w-4xl mx-auto p-6 shadow-lg">
      <!-- Gambar Produk -->
      <img
        v-if="post.meta.image"
        :src="post.meta.image"
        :alt="post.title"
        class="w-full h-72 object-cover rounded-lg mb-6"
      />

      <!-- Info Produk -->
      <div class="mb-6 text-center">
        <h1 class="text-4xl font-bold mb-2">{{ post.title }}</h1>
        <p class="text-primary font-semibold text-2xl">{{ post.price }}</p>
      </div>

      <!-- Deskripsi Produk -->
      <div class="prose max-w-none">
        <ContentRenderer :value="post" />
      </div>

      <!-- Tombol WhatsApp -->
      <div class="mt-8 text-center">
        <UButton size="lg" color="primary" icon="i-mdi-whatsapp" @click="goToWhatsApp"> Pesan Sekarang </UButton>
      </div>
    </UCard>
  </UContainer>
</template>

<style scoped>
.text-primary {
  color: #1e88e5;
}
.prose :where(img) {
  border-radius: 0.5rem;
}
</style>
