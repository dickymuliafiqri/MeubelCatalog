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
  <UNavigationMenu
    :items="items"
    :ui="{
      list: 'gap-5',
    }"
    class="w-full justify-center min-h-24"
  />
</template>
