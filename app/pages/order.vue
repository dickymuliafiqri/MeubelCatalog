<template>
  <div>
    <!-- Hero -->
    <section class="bg-gray-100 py-12 text-center">
      <UContainer>
        <h1 class="text-3xl md:text-4xl font-bold mb-4">Cara Pemesanan</h1>
        <p class="text-gray-600 max-w-2xl mx-auto">
          Ikuti langkah mudah berikut untuk memesan produk furniture impian Anda dari MeubelIndah.
        </p>
      </UContainer>
    </section>

    <!-- Steps -->
    <section class="py-16">
      <UContainer>
        <UGrid :columns="[1, 2, 3]" gap="6">
          <UCard v-for="(step, index) in steps" :key="index" class="text-center p-6">
            <div class="text-4xl font-bold text-primary mb-4">{{ index + 1 }}</div>
            <h3 class="font-semibold text-lg mb-2">{{ step.title }}</h3>
            <p class="text-gray-600">{{ step.description }}</p>
          </UCard>
        </UGrid>
      </UContainer>
    </section>

    <!-- Notes -->
    <section class="bg-gray-50 py-12">
      <UContainer>
        <h2 class="text-xl font-semibold mb-4">Catatan Penting</h2>
        <ul class="list-disc list-inside text-gray-600 space-y-2">
          <li>Waktu produksi ± 7-14 hari kerja tergantung jenis pesanan.</li>
          <li>Ongkos kirim ditanggung pembeli, disesuaikan dengan lokasi pengiriman.</li>
          <li>Pembayaran DP minimal 50% dari total harga.</li>
        </ul>
      </UContainer>
    </section>

    <!-- CTA -->
    <section class="bg-primary-500 text-white py-16 text-center">
      <UContainer>
        <h2 class="text-2xl font-bold mb-4">Siap Memesan?</h2>
        <p class="mb-6">Klik tombol di bawah untuk langsung terhubung dengan kami via WhatsApp.</p>
        <UButton size="lg" variant="solid" color="white" class="text-primary-500" :to="whatsappLink" target="_blank">
          Hubungi via WhatsApp
        </UButton>
      </UContainer>
    </section>
  </div>
</template>

<script setup>
const steps = [
  {
    title: "Pilih Produk",
    description: "Telusuri katalog dan tentukan produk yang ingin Anda beli.",
  },
  {
    title: "Hubungi Kami",
    description: "Kirim detail pesanan ke WhatsApp kami untuk konfirmasi stok dan harga.",
  },
  {
    title: "Lakukan Pembayaran",
    description: "Transfer DP atau pembayaran penuh, lalu pesanan akan segera diproses.",
  },
];

// Ganti nomor WhatsApp dengan nomor usaha kamu
const whatsappNumber = "6281234567890";
const whatsappMessage = "Halo, saya ingin memesan produk dari MeubelIndah.";
const whatsappLink = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(whatsappMessage)}`;
</script>

<style scoped>
.bg-primary-500 {
  background-color: #1e88e5;
}
.text-primary {
  color: #1e88e5;
}
</style>
