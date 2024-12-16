<script setup lang="ts">
</script>

<template>
    <div class="container mx-auto px-4 py-10">
      <!-- Success Message -->
      <div class="bg-green-50 border border-green-200 rounded-lg shadow text-center p-6 max-w-lg mx-auto">
        <h1 class="text-4xl font-bold text-green-600">Order Confirmed!</h1>
        <p class="text-gray-600 mt-4">
          Thank you for your purchase! Your order has been placed successfully.
        </p>
        <p class="text-gray-600 mt-2">Order ID: <span class="font-bold">#123456</span></p>
      </div>

      <!-- Actions -->
      <div class="flex justify-center space-x-4 mt-8">
        <router-link
            to="/"
            class="bg-gray-300 px-4 py-2 text-gray-800 rounded hover:bg-gray-400 transition"
        >
          Go Back Home
        </router-link>
        <router-link
            to="/details/123456"
            class="bg-blue-600 px-6 py-2 text-white rounded hover:bg-blue-500 transition"
        >
          View Order Details
        </router-link>
      </div>
    </div>
</template>