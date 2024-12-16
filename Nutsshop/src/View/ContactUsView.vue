<script lang="ts" setup>
const handleSubmit = () => {}
</script>
<template>
  <div class="container mx-auto p-6 max-w-lg">
    <h1 class="text-3xl font-bold text-blue-600 mb-6">Contact Us</h1>
    <form @submit.prevent="handleSubmit" class="space-y-4">
      <div>
        <label for="name" class="block text-gray-700 font-medium">Name</label>
        <input
            id="name"
            type="text"
            class="w-full p-3 border rounded focus:ring focus:ring-blue-200"
            placeholder="Your Name"
        />
      </div>
      <div>
        <label for="email" class="block text-gray-700 font-medium">Email</label>
        <input
            id="email"
            type="email"
            class="w-full p-3 border rounded focus:ring focus:ring-blue-200"
            placeholder="Your Email"
        />
      </div>
      <div>
        <label for="message" class="block text-gray-700 font-medium">Message</label>
        <textarea
            id="message"
            rows="4"
            class="w-full p-3 border rounded focus:ring focus:ring-blue-200"
            placeholder="Your Message"
        ></textarea>
      </div>
      <button
          type="submit"
          class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-500 transition-all"
      >
        Send Message
      </button>
    </form>
  </div>
</template>