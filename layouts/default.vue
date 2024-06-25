<template>
    <div>
        <header>
            <nav class="container mx-auto p-4 flex justify-between">
                <h2 class="shadow-sm bg-white font-bold"><nuxt-link to="/">Nuxt Dev</nuxt-link></h2>
                <ul class="flex gap-4">
                    <li><nuxt-link to="/">Home</nuxt-link></li>
                    <li><nuxt-link to="/about">About</nuxt-link></li>
                    <li><nuxt-link to="/products">Products</nuxt-link></li>
                </ul>
            </nav>
        </header>
    </div>

    <!-- output content -->
     <div class="container mx-auto px-4">
        <slot/>
     </div>
</template>

<script setup>

</script>

<style scoped>
.router-link-exact-active{
    color: rgb(144, 240, 245);
}
</style>