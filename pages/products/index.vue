<template>
    <div>
        <h2>Products Page</h2>
        <div class="grid grid-cols-4 gap-4">
            <div v-for="p in products" :key="p.id" >
                <nuxt-link :to="`/products/${p.id}`">
                    <h3>{{ p.title }}</h3>
                    <img width="200px" height="200px" :src="p.image" alt="">
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script setup>
// import Products from '../../layouts/products.vue';

definePageMeta({
    layout:'default'
})

const {data:products} = await useFetch('https://fakestoreapi.com/products')
console.log('data:', products.links);
</script>

<style lang="scss" scoped>

</style>