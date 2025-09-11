<template>
  <div class="container mx-auto px-4 py-24" un-cloak>
    <el-card body-class="h-96 flex flex-col items-center justify-center text-center">
      <div :class="i" class="size-12"></div>
      <h2>{{ title }}</h2>
      <p>{{ description }}</p>
    </el-card>
  </div>
</template>
<script setup>
import { inject } from "vue";
const { pid } = defineProps(["pid"]),
  pages = inject("pages"),
  { i, title, description } = pages[pid];
</script>
