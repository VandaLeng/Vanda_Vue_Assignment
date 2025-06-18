<template>
  <div class="bg-white p-6 rounded-lg shadow-md">
    <h2 class="text-3xl font-bold mb-4 text-red-600">Welcome to La Vespa</h2>
    <p class="text-lg mb-4">Explore our range of stylish Vespa scooters and accessories. Start your journey today!</p>
    <button @click="exploreProducts" class="bg-red-600 text-white px-4 py-2 rounded hover:bg-red-700 transition">
      Shop Now
    </button>
    <!-- test link page  -->
    <!-- <button @click="exploreContact" class="bg-red-600 text-white px-4 py-2 rounded hover:bg-red-700 transition">
      Shop Now
    </button> -->
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();

const exploreProducts = () => {
  router.push('/product');
};
// const exploreContact = () => {
//   router.push('/contact');
// };
</script>

<style scoped>
</style>