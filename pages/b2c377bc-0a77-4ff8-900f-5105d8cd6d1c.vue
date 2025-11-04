<template>
  <div class="container mx-auto px-4 py-24 text-center" un-cloak>
    <h3>{{ title }}</h3>
    <p class="mb-24">{{ description }}</p>
    <div class="grid grid-cols-4 gap-6 gap-y-12 lg:grid-cols-12 not-prose">
      <div class="col-span-4 flex flex-col items-center text-center" v-for="({ name, text }, index) in features">
        <div class="size-6 text-emerald-500" :class="`i-mdi:numeric-${index + 1}-circle-outline`"></div>
        <h3 class="my-4 text-lg leading-6 text-slate-700">{{ name }}</h3>
        <p class="text-slate-500">{{ text }}</p>
      </div>
    </div>
  </div>
</template>
<script setup>
import { inject } from "vue";
const { id } = defineProps(["id"]),
  pages = inject("pages"),
  { title, description } = pages[id],
  features = [
    {
      name: "The Simplest Website",
      text: "We create the simplest website using VueBro",
    },
    {
      name: "The Fastest Website",
      text: "We build websites on VueBro very quickly",
    },
    {
      name: "The Most Technologically Advanced Website",
      text: "We create websites using the latest technologies",
    },
  ];
</script>
