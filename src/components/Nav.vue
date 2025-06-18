<template>
  <nav class="flex justify-between items-center bg-blue-800 text-white p-4 rounded w-[1500px] m-auto">
    <!-- Left side: Logo and Branch Name -->
    <div class="flex items-center gap-4">
      <img src="/src/assets/Vespa.jpg" alt="Logo" class="w-16 h-16 rounded-full" />
      <h1 class="text-xl font-semibold">La Vespa</h1>
    </div>

    <!-- Right side: Navigation Links -->
    <div class="flex gap-6">
      <router-link
        v-for="item in navItems"
        :key="item.path"
        :to="item.path"
        class="hover:underline flex items-center gap-1"
      >
        <span class="material-symbols-outlined">{{ item.icon }}</span>
        {{ item.label }}
      </router-link>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const navItems = ref([
  { label: "Home", path: "/", icon: "home" },
  { label: "About", path: "/about", icon: "info" },
  { label: "Service", path: "/service", icon: "build" },
  { label: "Product", path: "/product", icon: "shopping_bag" },
  { label: "Contact", path: "/contact", icon: "call" },
]);
</script>

<style scoped>
.material-symbols-outlined {
  font-variation-settings:
    'FILL' 0,
    'wght' 400,
    'GRAD' 0,
    'opsz' 24;
}
</style>
