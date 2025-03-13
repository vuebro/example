<template>
  <div class="container mx-auto px-4 py-24">
    <h3 class="text-center">{{ title }}</h3>
    <p class="text-center mb-12">{{ description }}</p>
    <p v-for="paragraph in text" class="text-justify">{{ paragraph }}</p>
  </div>
</template>

<script setup>
import { inject } from "vue";
import { getParagraph } from "speech-code";

const { id } = defineProps(["id"]),
  { title, description } = inject("pages")[id],
  text = Array(12).fill().map(() => getParagraph());
</script>
