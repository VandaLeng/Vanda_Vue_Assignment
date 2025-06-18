<template>
  <div class="bg-white p-6 rounded-lg shadow-md">
    <h2 class="text-3xl font-bold mb-4 text-red-600">Contact Us</h2>
    <p class="text-lg mb-4">Email: info@lavespa.com | Phone: +1-123-456-7890</p>
    <div class="mt-4">
      <input v-model="message" type="text" placeholder="Your message" class="border p-2 rounded w-full mb-2">
      <button @click="sendMessage" class="bg-red-600 text-white px-4 py-2 rounded hover:bg-red-700 transition">
        Send Message
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const message = ref('');

const sendMessage = () => {
  if (message.value.trim()) {
    alert('Message sent: ' + message.value);
    message.value = '';
  } else {
    alert('Please enter a message.');
  }
};
</script>

<style scoped>
</style>