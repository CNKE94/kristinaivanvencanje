<script setup lang="ts">
interface Props {
  heading: string;
  icon?: string;
  time: string;
  place: string;
  address: string;
  src?: string;
}
defineProps<Props>();
</script>

<template>
    <div class="flex flex-col px-10 pt-10 pb-4 bg-white rounded-lg text-center gap-y-4">
        <AppHeading class="text-3xl font-bold" heading="h2" :title="heading" />
        <NuxtImg :src="icon" alt="icon" class="w-20 mx-auto" />
        <p class="text-lg font-semibold">{{ time }}</p>
        <p class="text-2xl">{{ place }}</p>
        <p>{{ address }}</p>
        <NuxtLink
         :to="src" 
         target="_blank"
         class="flex justify-center gap-x-2 p-2 rounded-lg text-white bg-orange-400 my-6 hover:opacity-85"
        >
        <NuxtImg src="images/location.svg" alt="icon" class="text-white w-5" />
         Нађи на мапи
        </NuxtLink>
    </div>
</template>