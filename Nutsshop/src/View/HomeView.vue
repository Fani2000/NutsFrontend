<script setup lang="ts">
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
    <div class="px-6 h-[330px] mb-6 bg-[url('./assets/images/background.svg')]">
      <div class="relative top-10 flex flex-col gap-20 text-white bg-gradient-to-b from-transparent">
        <div class="flex justify-between">
          <div>
            <img src="../assets/Images/logo.svg" />
          </div>
          <div class="flex gap-6">
            <div>
              <img src="../assets/Images/search.svg" />
            </div>
            <div>
              <img src="../assets/Images/cart.svg" />
            </div>
          </div>
        </div>
        <div class="">
          <h1 class="text-4xl font-bold">Discover Nature's Bounty</h1>
          <p class="text-xl mt-2">
            Discover our premium selection of fresh and healthy nuts just for you!
          </p>
          <p class="mt-2">
            Fuel your body and mind with nature's most delicious energy source.
            Explore our wide variety of nuts and discover the perfect fit for your
            healthy lifestyle.
          </p>
        </div>
      </div>
    </div>

    <!-- Product Grid -->
    <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <!-- Product Card -->
      <div v-for="product in products" :key="product.id"
        class="bg-white shadow rounded overflow-hidden group hover:shadow-lg transition-shadow">
        <!-- Image -->
        <img :src="product.image" :alt="product.name" class="w-full h-48 object-cover" />

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