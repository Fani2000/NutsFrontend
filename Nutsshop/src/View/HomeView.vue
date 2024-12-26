<script setup lang="ts">
import Header from '../Components/Header.vue'
// Example sample data for nuts products
const products = [
  {
    id: 1,
    name: "Almonds",
    description: "Rich in nutrients, an excellent source of fiber and healthy fats.",
    image: "https://via.placeholder.com/300x200?text=Almonds",
    tags: ["Healthy", "Fiber", "Energy"],
  },
  {
    id: 2,
    name: "Cashews",
    description: "A delicious, creamy snack packed with essential vitamins.",
    image: "https://via.placeholder.com/300x200?text=Cashews",
    tags: ["Creamy", "Snack", "Magnesium"],
  },
  {
    id: 3,
    name: "Walnuts",
    description: "Boosts brain health, a perfect source of omega-3 fatty acids.",
    image: "https://via.placeholder.com/300x200?text=Walnuts",
    tags: ["Omega-3", "Brain Food", "Crunchy"],
  },
];
</script>

<template>
  <div>
    <!-- Heading -->
    <Header />

    <!-- Product Grid -->
    <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <!-- Product Card -->
      <div v-for="product in products" :key="product.id"
        class="bg-white shadow rounded overflow-hidden group hover:shadow-lg transition-shadow">
        <!-- Image -->
        <img src="../assets/products/mixed-nuts.svg" :alt="product.name" class="w-full h-48 object-cover" />

        <!-- Content -->
        <div class="p-4">
          <h3 class="text-lg font-bold text-blue-600">{{ product.name }}</h3>
          <p class="text-gray-600 mt-2">{{ product.description }}</p>

          <!-- Tags -->
          <div class="flex flex-wrap mt-4 space-x-2">
            <span v-for="tag in product.tags" :key="tag" class="bg-blue-100 text-blue-600 text-sm px-3 py-1 rounded-full">
              {{ tag }}
            </span>
          </div>
        </div>

        <!-- View Details Button -->
        <div class="p-4 border-t text-right">
          <router-link :to="'/products/' + product.id"
            class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-500 transition-all">
            View Details
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>