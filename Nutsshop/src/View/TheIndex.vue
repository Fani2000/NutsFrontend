<script setup lang="ts">
import TheIndex from "./View/TheIndex.vue";
</script>

<template>
  <div class="flex flex-col min-h-screen">
    <!-- Header -->
    <header class="bg-white shadow-md sticky top-0 z-10">
      <nav class="flex justify-between items-center px-6 py-3">
        <h1 class="text-2xl text-blue-600 font-bold">My App</h1>
        <div class="flex space-x-4">
          <router-link
              to="/"
              class="text-gray-700 hover:text-blue-600 transition-colors"
          >
            Home
          </router-link>
          <router-link
              to="/contact"
              class="text-gray-700 hover:text-blue-600 transition-colors"
          >
            Contact
          </router-link>
        </div>
      </nav>
    </header>

    <!-- Main Content: Router View -->
    <main class="flex-grow bg-gray-100 p-6">
      <router-view />
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-center text-white py-3">
      © 2023 My Company - All Rights Reserved
    </footer>
  </div>
</template>

<style scoped>
/* Add any additional customization styles here if needed */
</style>