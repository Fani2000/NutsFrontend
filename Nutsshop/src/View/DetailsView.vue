<script setup lang="ts">
</script>

<template>
  <div class="container mx-auto px-4 py-10">
    <!-- Header Section -->
    <div class="text-center">
      <h1 class="text-4xl font-bold text-blue-600">Product Details</h1>
      <p class="text-gray-600 mt-2">
        Find all the important information about your selected product here.
      </p>
    </div>

    <!-- Details Card -->
    <div class="bg-white shadow rounded-lg p-6 mt-10 max-w-xl mx-auto">
      <!-- Product Image -->
      <img src="../assets/products/nuts-details.svg" alt="Product" class="w-full h-60 object-cover rounded" />

      <!-- Product Info -->
      <div class="mt-6">
        <h2 class="text-2xl font-bold text-blue-600">Almonds</h2>
        <p class="text-gray-700 mt-2">
          Almonds are a rich source of healthy fats, fiber, and protein.
          Perfect for snacking and a great addition to your diet!
        </p>

        <!-- Product Tags -->
        <div class="flex flex-wrap mt-4 space-x-2">
          <span class="bg-blue-100 text-blue-600 text-sm px-3 py-1 rounded-full">
            Healthy
          </span>
          <span class="bg-blue-100 text-blue-600 text-sm px-3 py-1 rounded-full">
            Fiber
          </span>
          <span class="bg-blue-100 text-blue-600 text-sm px-3 py-1 rounded-full">
            Energy
          </span>
        </div>
      </div>

      <!-- Action Section -->
      <div class="mt-6 flex space-x-4">
        <router-link to="/add-to-cart" class="px-4 py-2 rounded transition">
          <button type="button" class="bg-blue-600 px-6 py-2 text-white rounded hover:bg-blue-500 transition">
            Add to Cart
          </button>
        </router-link>
      </div>
    </div>
  </div>
</template>