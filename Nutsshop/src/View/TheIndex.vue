<script setup lang="ts">
</script>

<template>
  <div class="flex flex-col min-h-screen">

    <!-- Main Content: Router View -->
    <main class="flex-grow bg-gray-100">
      <router-view />
    </main>

    <!-- Footer -->
    <footer class="bg-[#070F2B] text-white py-3 h-38">
      <div class="flex flex-col items-center py-6">
        <div>Home</div>
        <div>Contact us</div>
        <div>About us</div>
        <div>© 2023 NutShop - All Rights Reserved</div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
/* Add any additional customization styles here if needed */
</style>