<script setup lang="ts">
import { useRuntimeConfig } from "#imports";
const runtimeConfig = useRuntimeConfig();

useHead({
  htmlAttrs: {
    lang: "en",
  },
  link: [
    {
      rel: "icon",
      type: "image/x-icon",
      href: "/kristinaivanvencanje/images/wedding-couple.svg",
    },
  ],
});

useSeoMeta({
  title: "Кристина & Иван",
  description: "Позивница за Венчање",
  charset: "utf-8",
  viewport: "width=device-width, initial-scale=1",
  ogImage: {
    url: `https://cnke94.github.io/kristinaivanvencanje/images/vencanje.jpg`,
    width: 1200,
    height: 630,
    type: "image/jpeg",
  },
});
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
