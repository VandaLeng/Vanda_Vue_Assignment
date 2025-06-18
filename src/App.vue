<template>
  <div class="flex items-center gap-4 bg-amber-200 w-[1500px] m-auto p-4 rounded">
    <img src="/src/assets/Vespa.jpg" alt="Logo" class="w-16 h-16 rounded-full" />

    <h1 class="text-xl font-semibold">
      La Vespa
    </h1>
  </div>

  <WelcomeItemVue />
</template>

<script setup>
import WelcomeItemVue from "./components/Todo.vue";
</script>

<style scoped>
</style>
