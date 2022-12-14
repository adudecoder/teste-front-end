<template>
    <div>
        <section class="text-gray-600 body-font">
            <div class="container px-5 py-24 mx-auto">
                <div class="flex flex-wrap -m-4">
                    <div class="lg:w-1/4 md:w-1/2 p-4 w-full" v-for="product in products">
                        <ProductCard :product="product" />
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
    // fetch the products
    const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped>
.router-link-exact-active {
    color: #12b488;
}
</style>