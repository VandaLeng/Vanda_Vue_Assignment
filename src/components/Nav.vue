<template>
  <nav class="flex gap-6 bg-blue-800 text-white p-2 rounded justify-center ">
        <!-- Logo and Name Section -->
    <div class="flex items-center gap-4 rounded ">
      <img src="/src/assets/Vespa.jpg" alt="Logo" class="w-16 h-16 rounded-full" />
      <h1 class="text-xl font-semibold">La Vespa</h1>
    </div>
    <router-link
      v-for="item in navItems"
      :key="item.path"
      :to="item.path"
      class="hover:underline flex items-center gap-1"
    >
      <span class="material-icons">{{ item.icon }}</span>
      {{ item.label }}
    </router-link>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const navItems = ref([
  { label: "Home", path: "/", icon: "home" },
  { label: "About", path: "/about", icon: "info" },
  { label: "Service", path: "/service", icon: "build" },
  { label: "Product", path: "/product", icon: "local_mall" },
  { label: "Contact", path: "/contact", icon: "contacts" },
]);
</script>

<style scoped>
@import url('https://fonts.googleapis.com/icon?family=Material+Icons');
</style>
