<script setup lang="ts">
import Header from '../Components/Header.vue'
import ProductCart from '../Components/ProductCart.vue';
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
  {
    id: 4,
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
    <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 pb-10">
      <!-- Product Card -->
      <ProductCart :products="[...products, ...products, ...products]" />
    </div>
  </div>
</template>