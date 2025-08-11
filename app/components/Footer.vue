<template>
  <footer class="bg-gray-900 text-white py-10 mt-12">
    <UContainer>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Info Usaha -->
        <div>
          <h3 class="text-xl font-bold mb-4">Meubel Abadi Suar Jaya</h3>
          <p>Dusun Krajan RT/RW 001/005 Desa PURWOHARJO 68483</p>
          <p>Banyuwangi, Jawa Timur</p>
          <p>Email: abadisuarjaya@gmail.com</p>
          <p>Telp: +62 852-9477-5689</p>
        </div>

        <!-- Metode Pembayaran -->
        <div>
          <h3 class="text-xl font-bold mb-4">Metode Pembayaran</h3>
          <div class="flex flex-wrap items-center gap-4">
            <img src="/images/bank/bca.png" alt="BCA" class="h-8 object-contain" />
          </div>
        </div>

        <!-- Media Sosial -->
        <div>
          <h3 class="text-xl font-bold mb-4">Ikuti Kami</h3>
          <div class="flex flex-wrap items-center gap-4">
            <NuxtLink to="https://www.instagram.com/abadisuarjaya?igsh=bjVmbTNhbWk3bXRh&utm_source=qr" target="_blank">
              <img src="/images/logo/instagram.png" alt="Instagram" class="h-8 object-contain" />
            </NuxtLink>
          </div>
        </div>
      </div>

      <!-- Copyright -->
      <div class="mt-8 border-t border-gray-700 pt-4 text-center text-sm">
        &copy; {{ new Date().getFullYear() }} Toko Mebel Abadi Suar Jaya. Semua Hak Dilindungi.
      </div>
    </UContainer>
  </footer>
</template>

<script setup lang="ts">
// Tidak ada script khusus, cukup static footer
</script>

<style scoped>
footer img {
  filter: brightness(0) invert(1); /* agar logo bank putih */
}
</style>
