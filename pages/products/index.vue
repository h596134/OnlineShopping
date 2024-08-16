<!-- HTML -->
<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
        <div v-for="p in products">
            <ProductCard :product="p"/>
            </div>
        </div>
    </div>
</template>

<!-- Code -->
<script setup>
definePageMeta({
    layout: 'products'
})
// fetch products from fake endpoint api
const {data: products} = await useFetch('https://fakestoreapi.com/products')
</script>

<!-- CSS -->
<style scoped>
 h2 {
    font-size: 36px
 }
 p {
    margin: 20px 0;
 }
</style>