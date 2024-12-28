<script setup lang="ts">

// Example order details
const order = {
  id: "123456",
  date: "2023-10-10",
  total: 78.76,
  items: [
    {
      id: 1,
      name: "Almonds",
      quantity: 2,
      price: 15.99,
      image: "https://via.placeholder.com/150?text=Almonds",
    },
    {
      id: 2,
      name: "Cashews",
      quantity: 1,
      price: 12.49,
      image: "https://via.placeholder.com/150?text=Cashews",
    },
    {
      id: 3,
      name: "Walnuts",
      quantity: 3,
      price: 18.29,
      image: "https://via.placeholder.com/150?text=Walnuts",
    },
  ],
};
</script>

<template>
  <div class="container mx-auto px-4 py-10">
    <!-- Order Header -->
    <div class="text-center">
      <h1 class="text-4xl font-bold text-green-600">Order Details</h1>
      <p class="text-gray-600 mt-2">Order ID: <span class="font-bold">{{ order.id }}</span></p>
      <p class="text-gray-600">Order Date: {{ order.date }}</p>
    </div>

    <!-- Order Items -->
    <div class="bg-white shadow rounded-lg p-6 mt-8">
      <div v-for="item in order.items" :key="item.id"
        class="flex items-center justify-between border-b py-4 last:border-b-0">
        <!-- Product Info -->
        <div class="flex items-center space-x-4">
          <img src="../assets/products/mixed-nuts.svg" :alt="item.name" class="w-16 h-16 object-cover rounded" />
          <div>
            <h3 class="font-bold text-lg text-green-600">{{ item.name }}</h3>
            <p class="text-gray-600">Qty: {{ item.quantity }}</p>
          </div>
        </div>

        <!-- Price -->
        <p class="text-lg font-bold text-gray-700">${{ (item.price * item.quantity).toFixed(2) }}</p>
      </div>
    </div>

    <!-- Order Summary -->
    <div class="bg-gray-100 shadow-lg rounded-lg p-6 mt-6 max-w-md mx-auto">
      <div class="flex justify-between items-center">
        <p class="text-lg font-medium text-gray-600">Total To Be Paid</p>
        <p class="text-2xl font-bold text-gray-800">${{ order.total }}</p>
      </div>

      <!-- Actions -->
      <div class="mt-6 flex justify-center">
        <router-link to="/confirmation" class="px-4 py-2 rounded transition">
          <button type="button" class="bg-green-600 px-6 py-2 text-white rounded hover:bg-green-500 transition">
            Confirm Order
          </button>
        </router-link>
        <router-link to="/" class="px-4 py-2 rounded transition">
          <button type="button" class="bg-green-600 px-6 py-2 text-white rounded hover:bg-green-500 transition">
            Back To Home
          </button>
        </router-link>
      </div>
    </div>
  </div>
</template>