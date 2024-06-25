<template>
    <div>
        <header>
            <h3>Products Page Layout</h3>
        </header>
    </div>

    <!-- output content -->
     <div>
        <slot/>
     </div>

     <footer>
        <nav>
            <ul>
                <li><nuxt-link to="/">Home</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
                <li><nuxt-link to="/products">Products</nuxt-link></li>
            </ul>
        </nav>
     </footer>
     
</template>

<script setup>
definePageMeta({
    layout:'default'
})

</script>

<style scoped>
.router-link-exact-active{
    color: rgb(144, 240, 245);
}
</style>