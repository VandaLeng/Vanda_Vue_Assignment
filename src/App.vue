<template>
  <div class="w-[1500px] m-auto">
    <NavVue />

    <div class="bg-amber-200 p-4 rounded mt-4">
      <router-view></router-view>
    </div>
  </div>
</template>

<script setup>
import NavVue from "./components/Nav.vue";
</script>

<style scoped>
</style>
