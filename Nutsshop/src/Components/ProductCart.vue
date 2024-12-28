<template>
    <div v-for="product in products" :key="product.id"
        class="bg-white shadow rounded overflow-hidden group hover:shadow-lg transition-shadow">
        <!-- Image -->
        <img src="../assets/products/mixed-nuts.svg" :alt="product.name" class="w-full h-48 object-cover" />

        <!-- Content -->
        <div class="p-4">
            <h3 class="text-lg font-bold text-green-600">{{ product.name }}</h3>
            <p class="text-gray-600 mt-2">{{ product.description }}</p>

            <!-- Tags -->
            <div class="flex flex-wrap mt-4 space-x-2">
                <span v-for="tag in product.tags" :key="tag"
                    class="bg-blue-100 text-green-600 text-sm px-3 py-1 rounded-full">
                    {{ tag }}
                </span>
            </div>
        </div>

        <!-- View Details Button -->
        <div class="p-4 border-t text-right">
            <router-link :to="'/products/' + product.id"
                class="bg-green-600 text-white px-4 py-2 rounded hover:bg-green-500 transition-all">
                View Details
            </router-link>
        </div>
    </div>
</template>
<script setup lang="ts">
import { PropType } from 'vue'
defineProps({
    products: Array as PropType<any>
})
</script>