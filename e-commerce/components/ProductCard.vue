<template>

    <a class="block relative rounded overflow-hidden bg-gray-100">
        <img alt="ecommerce" class="thumb object-cover object-center w-full h-full block" :src="product.image">
    </a>
    <div class="mt-4">
        <h3 class="text-gray-500 text-xs tracking-widest title-font mb-1">
            {{ product.category }}
        </h3>
        <h2 class="text-gray-900 title-font text-lg font-medium">
            <nuxt-link :to="`/products/${product.id}`"> {{ product.title }} </nuxt-link>
        </h2>
        <p class="mt-1">$ - {{ product.price }}</p>
    </div>
    <nuxt-link :to="`/products/${product.id}`">
        <p class="btn my-4">View Details</p>
    </nuxt-link>

</template>

<script setup>
const { product } = defineProps(['product'])
</script>

<style scoped>
.thumb {
    max-height: 120px;
    max-width: 100px;
    margin: 0 auto;
}
</style>

