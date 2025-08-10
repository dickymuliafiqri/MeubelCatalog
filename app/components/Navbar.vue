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
  <div class="w-full h-max py-3 flex justify-center items-center">
    <img src="/images/logo/main.png" alt="Logo" class="w-36" />
  </div>
  <UNavigationMenu
    :items="items"
    :ui="{
      list: 'gap-5',
    }"
    class="w-full justify-center min-h-16"
  />
</template>
