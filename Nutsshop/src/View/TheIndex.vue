<script setup lang="ts">
</script>

<template>
  <div class="flex flex-col min-h-screen">
    
    <!-- Main Content: Router View -->
    <main class="flex-grow bg-gray-100">
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