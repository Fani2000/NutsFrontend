<script setup lang="ts">
</script>

<template>
  <div class="flex flex-col min-h-screen">

    <!-- Main Content: Router View -->
    <main class="flex-grow bg-gray-100">
      <router-view />
    </main>

    <!-- Footer -->
    <footer class="bg-[#070F2B] text-white py-3 mt-10 h-56">
      <div class="flex flex-col items-center py-6">
        <div>Links</div>
        <div>© 2023 My Company - All Rights Reserved</div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
/* Add any additional customization styles here if needed */
</style>