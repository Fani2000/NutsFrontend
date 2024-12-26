<script setup lang="ts">

// Example cart items
const cartItems = [
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
];

// Calculate total price
const totalPrice = cartItems.reduce((sum, item) => sum + item.price * item.quantity, 0).toFixed(2);
</script>

<template>
    <div class="container mx-auto px-4 py-10">
      <!-- Header -->
      <h1 class="text-4xl font-bold text-blue-600 text-center">Your Cart</h1>
      <p class="text-gray-600 text-center mt-2">
        Review and manage the items in your cart before checking out.
      </p>

      <!-- Cart Items -->
      <div class="mt-8 bg-white shadow rounded-lg p-6">
        <div
            v-for="item in cartItems"
            :key="item.id"
            class="flex items-center justify-between border-b py-4 last:border-b-0"
        >
          <!-- Product Info -->
          <div class="flex items-center space-x-4">
            <img
                src="../assets/products/mixed-nuts.svg"
                :alt="item.name"
                class="w-16 h-16 object-cover rounded"
            />
            <div>
              <h3 class="font-bold text-lg text-blue-600">{{ item.name }}</h3>
              <p class="text-gray-600">Qty: {{ item.quantity }}</p>
            </div>
          </div>

          <!-- Price -->
          <p class="text-lg font-bold text-gray-700">${{ (item.price * item.quantity).toFixed(2) }}</p>
        </div>
      </div>

      <!-- Cart Summary -->
      <div class="bg-gray-100 shadow-lg rounded-lg p-6 mt-6 max-w-md mx-auto">
        <div class="flex justify-between items-center">
          <p class="text-lg font-medium text-gray-600">Total Price</p>
          <p class="text-2xl font-bold text-gray-800">${{ totalPrice }}</p>
        </div>

        <!-- Actions -->
        <div class="mt-6 flex justify-between space-x-4">
          <router-link
              to="/"
              class="bg-gray-300 px-4 py-2 rounded text-gray-800 hover:bg-gray-400 transition"
          >
            Continue Shopping
          </router-link>
          <router-link
              to="/order-details"
              class="bg-blue-600 px-6 py-2 text-white rounded hover:bg-blue-500 transition"
          >
            Proceed to Checkout
          </router-link>
        </div>
      </div>
    </div>
</template>