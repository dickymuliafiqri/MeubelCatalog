<template>
  <div>
    <!-- Hero Section -->
    <section
      class="relative bg-gray-100 min-w-screen lg:min-h-screen flex justify-center items-center flex-col overflow-hidden"
    >
      <div
        class="w-full h-full absolute overflow-hidden flex justify-center items-center bg-cover bg-[url(https://media.johnlewiscontent.com/i/johnlewis/Small-space-furniture-lead)]"
      ></div>
      <UContainer
        class="py-5 text-center z-10 rounded-xl backdrop-blur-xs lg:backdrop-blur-sm text-white flex justify-center items-center flex-col"
      >
        <img src="/images/logo/asj.png" alt="Abadi Suar Jaya" class="w-48" />
        <h1 class="text-3xl md:text-5xl font-bold mb-4">Furniture Elegan, Nyaman, & Berkualitas</h1>
        <p class="mb-6">
          Kami menyediakan berbagai pilihan meubel untuk rumah dan kantor dengan desain modern dan harga bersahabat.
        </p>
        <UButton size="lg" to="/catalog" variant="solid" color="primary"> Lihat Katalog </UButton>
      </UContainer>
    </section>

    <!-- Tentang Usaha -->
    <section id="tentang" class="py-16">
      <UContainer>
        <h2 class="text-2xl font-semibold mb-4 text-center">Tentang Kami</h2>
        <p class="text-gray-600 max-w-3xl mx-auto text-center">
          MeubelIndah berdiri sejak 2010, berkomitmen menyediakan produk meubel berkualitas tinggi yang tahan lama.
          Dengan tenaga kerja profesional, kami memastikan setiap produk dibuat dengan teliti dan menggunakan bahan
          terbaik.
        </p>
      </UContainer>
    </section>

    <!-- Keunggulan Usaha -->
    <section class="bg-gray-50 py-16">
      <UContainer>
        <h2 class="text-2xl font-semibold mb-10 text-center">Kenapa Memilih Kami?</h2>
        <div
          v-for="item in advantages"
          :key="item.title"
          class="p-6 my-2 bg-white backdrop-blur-lg rounded-lg shadow text-center"
        >
          <div class="text-4xl mb-4">{{ item.icon }}</div>
          <h3 class="font-bold mb-2">{{ item.title }}</h3>
          <p class="text-gray-600">{{ item.description }}</p>
        </div>
      </UContainer>
    </section>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "home",
});

const advantages = [
  {
    icon: "🪵",
    title: "Bahan Berkualitas",
    description: "Menggunakan kayu pilihan dan material terbaik.",
  },
  {
    icon: "🎨",
    title: "Desain Modern",
    description: "Mengikuti tren terbaru untuk keindahan rumah Anda.",
  },
  {
    icon: "⚡",
    title: "Pengiriman Cepat",
    description: "Proses pengiriman aman dan tepat waktu.",
  },
];
</script>

<style scoped>
.bg-primary-500 {
  background-color: #1e88e5;
}
.text-primary-500 {
  color: #1e88e5;
}
</style>
