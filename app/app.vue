<template>
  <NuxtRouteAnnouncer />
  <UApp>
    <NuxtLayout>
      <NuxtPage></NuxtPage>
    </NuxtLayout>
  </UApp>
</template>

<script setup lang="ts">
const route = useRoute();
console.log(route.fullPath);

// SEO
useHead({
  title: "Abadi Suar Jaya | Meubel & Furniture Kayu Berkualitas di Banyuwangi",
  meta: [
    {
      name: "description",
      content:
        "Abadi Suar Jaya adalah toko meubel di Banyuwangi yang menyediakan furniture kayu solid berkualitas tinggi: meja, kursi, lemari, dan desain custom.",
    },
    {
      name: "keywords",
      content:
        "meubel Banyuwangi, toko furniture Banyuwangi, meubel kayu solid, Abadi Suar Jaya, furniture custom Banyuwangi, meja kayu, kursi kayu, lemari kayu",
    },
    { property: "og:title", content: "Abadi Suar Jaya | Meubel & Furniture Kayu Berkualitas di Banyuwangi" },
    {
      property: "og:description",
      content:
        "Toko meubel di Banyuwangi dengan koleksi furniture kayu solid, meja, kursi, lemari, dan custom design. Kualitas premium, harga terbaik.",
    },
    { property: "og:type", content: "business.business" },
    { property: "og:url", content: "https://www.abadisuarjaya.com" },
    { property: "og:image", content: "https://www.abadisuarjaya.com/thumbnail.jpg" },
    { name: "twitter:card", content: "summary_large_image" },
    { name: "twitter:title", content: "Abadi Suar Jaya | Meubel & Furniture Kayu Berkualitas di Banyuwangi" },
    {
      name: "twitter:description",
      content:
        "Abadi Suar Jaya menyediakan meubel kayu solid berkualitas tinggi di Banyuwangi. Tersedia meja, kursi, lemari, dan custom design.",
    },
    { name: "twitter:image", content: "https://www.abadisuarjaya.com/thumbnail.jpg" },
  ],
  link: [{ rel: "canonical", href: "https://www.abadisuarjaya.com" }],
  script: [
    {
      type: "application/ld+json",
      tagPosition: "head",
      innerHTML: JSON.stringify({
        "@context": "https://schema.org",
        "@type": "FurnitureStore",
        name: "Abadi Suar Jaya",
        image: "https://www.abadisuarjaya.com/thumbnail.jpg",
        "@id": "",
        url: "https://www.abadisuarjaya.com",
        telephone: "+62 852-9477-5689",
        priceRange: "Rp",
        address: {
          "@type": "PostalAddress",
          streetAddress: "Dusun Krajan RT/RW 001/005 Purwoharjo",
          addressLocality: "Banyuwangi",
          addressRegion: "Jawa Timur",
          postalCode: "68483",
          addressCountry: "ID",
        },
        geo: {
          "@type": "GeoCoordinates",
          latitude: -8.4889307,
          longitude: 114.2225106,
        },
        openingHoursSpecification: [
          {
            "@type": "OpeningHoursSpecification",
            dayOfWeek: ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"],
            opens: "08:00",
            closes: "17:00",
          },
        ],
        sameAs: ["https://www.facebook.com/abadisuarjaya", "https://www.instagram.com/abadisuarjaya"],
      }),
    },
  ],
});
</script>
