<template>
  <footer class="bg-gray-900 text-white py-10 mt-12">
    <UContainer>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Info Usaha -->
        <div>
          <h3 class="text-xl font-bold mb-4">Toko Mebel Indah</h3>
          <p>Jl. Melati No. 123</p>
          <p>Kota Bandung, Jawa Barat</p>
          <p>Email: tokomebel@example.com</p>
          <p>Telp: 0812-3456-7890</p>
        </div>

        <!-- Metode Pembayaran -->
        <div>
          <h3 class="text-xl font-bold mb-4">Metode Pembayaran</h3>
          <div class="flex flex-wrap items-center gap-4">
            <img src="/images/bank/bca.png" alt="BCA" class="h-8 object-contain" />
            <img src="/images/bank/mandiri.png" alt="Mandiri" class="h-8 object-contain" />
            <img src="/images/bank/bni.png" alt="BNI" class="h-8 object-contain" />
            <img src="/images/bank/bri.png" alt="BRI" class="h-8 object-contain" />
          </div>
        </div>

        <!-- Media Sosial -->
        <div>
          <h3 class="text-xl font-bold mb-4">Ikuti Kami</h3>
          <div class="flex flex-wrap items-center gap-4">
            <img src="/images/logo/instagram.png" alt="BCA" class="h-8 object-contain" />
            <img src="/images/logo/tiktok.png" alt="Mandiri" class="h-8 object-contain" />
          </div>
        </div>
      </div>

      <!-- Copyright -->
      <div class="mt-8 border-t border-gray-700 pt-4 text-center text-sm">
        &copy; {{ new Date().getFullYear() }} Toko Mebel Indah. Semua Hak Dilindungi.
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
