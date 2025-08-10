<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";
import { ref } from "vue";

const items = ref<NavigationMenuItem[]>([
  {
    label: "Home",
    to: "/",
  },
  {
    label: "Produk",
    to: "/catalog",
  },
  {
    label: "Cara Pemesanan",
    to: "/order",
  },
]);
</script>

<template>
  <div class="w-full h-max flex justify-center items-center">
    <img src="/images/logo/asj.png" alt="Logo" class="w-42" />
  </div>
  <UNavigationMenu
    :items="items"
    :ui="{
      list: 'gap-5',
    }"
    class="w-full justify-center min-h-16"
  />
</template>

<style scoped>
img {
  filter: brightness(0) invert(0); /* agar logo bank putih */
}
</style>
