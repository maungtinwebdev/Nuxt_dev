<template>
    <div>
        <h3>Product Details For {{ id }}</h3>
        <h3>{{ product.title }}</h3>
        <h3>{{ product }}</h3>
        <h3>Price: ${{ product.price }}</h3>
        <h3>{{ product.id }}</h3>
        <img width="200px" height="200px" :src="product.image" alt="">
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro, voluptas eveniet nobis vel harum illum velit vero asperiores ab necessitatibus?</p>
    </div>
</template>

<script setup>
    const { id } = useRoute().params

    const uri = 'https://fakestoreapi.com/products/'+ id

    const {data:product} = await useFetch(uri)

    definePageMeta({
        layout:'default'
    })
</script>

<style lang="scss" scoped>

</style>