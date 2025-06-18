<template>
  <div class="bg-white p-6 rounded-lg shadow-md">
    <h2 class="text-3xl font-bold mb-4 text-red-600">Our Services</h2>
    <p class="text-lg mb-4">Maintenance, repairs, and customization for your Vespa scooter. Book a service today!</p>
    <button @click="bookService" class="bg-red-600 text-white px-4 py-2 rounded hover:bg-red-700 transition">
      Book Now
    </button>
  </div>
</template>

<script setup>
const bookService = () => {
  alert('Service booking form would open here!');
};
</script>

<style scoped>
</style>