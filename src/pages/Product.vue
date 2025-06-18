<template>
  <div class="bg-white p-6 rounded-lg shadow-md">
    <h2 class="text-3xl font-bold mb-4 text-red-600">Our Products</h2>
    <p class="text-lg mb-4">Check out our latest Vespa models and accessories for sale. Ride in style!</p>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      <div v-for="(product, index) in products" :key="index" class="border rounded-lg p-4 hover:shadow-lg transition">
        <img :src="product.image" :alt="product.name" class="w-full h-48 object-cover rounded mb-2">
        <h3 class="text-xl font-semibold">{{ product.name }}</h3>
        <p class="text-gray-600">{{ product.price }}</p>
        <button @click="addToCart(product)" class="bg-red-600 text-white px-4 py-2 mt-2 rounded hover:bg-red-700 transition">
          Add to Cart
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const products = ref([
  { name: 'Vespa Primavera 150', price: '$5,499', image: 'https://via.placeholder.com/300x200?text=Primavera+150' },
  { name: 'Vespa Sprint 50', price: '$4,199', image: 'https://via.placeholder.com/300x200?text=Sprint+50' },
  { name: 'Vespa Helmet', price: '$199', image: 'https://via.placeholder.com/300x200?text=Helmet' },
]);

const addToCart = (product) => {
  alert(`Added ${product.name} to cart!`);
};
</script>

<style scoped>
</style>