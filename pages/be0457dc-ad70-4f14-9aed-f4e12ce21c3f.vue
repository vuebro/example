<template>
  <div class="min-h-dvh" un-cloak>
    <el-page-header :icon="AlarmClock" :content="pages[route.name].title" :title="title" @back="$router.push('/')"
      class="sticky top-0 z-50 pa-4 border-b bg-neutral-50"></el-page-header>
    <router-view></router-view>
  </div>
  <div class="flex flex-col gap-8 items-center bg-neutral-200 pa-12 not-prose" un-cloak>
    <el-button-group>
      <el-button v-for="child in $children" tag="router-link" :to="child.to">{{
        child.title
        }}</el-button>
    </el-button-group>
    <el-text>{{ description }}</el-text>
  </div>
</template>

<script setup>
import "https://unpkg.com/element-plus@2.9.6/dist/index.css";
import ElementPlus from "element-plus";
import { AlarmClock } from "@element-plus/icons-vue";
import { inject } from "vue";
import { useRoute } from "vue-router";

window.app.use(ElementPlus);
const { id } = defineProps(["id"]),
  pages = inject("pages"),
  { title, description, $children } = pages[id],
  route = useRoute();
</script>
