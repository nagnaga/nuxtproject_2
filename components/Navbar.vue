<script setup >

</script>
<template>
    <nav class="bg-gray-800">
        <div class="max-w-7x1 mx-auto px-2 sm:px-6 lg:px-8">
            <div class="relative flex items-center justify-between h-16">
                <div class="hidden sm:block sm:ml-6">
                    <div class="flex space-x-4">
                        <!-- Home Tab -->
                        <nuxt-link to="/"
                        class="text-white px-3 py-2 rounded-md text-sm
                        font-medium"
                        >Home</nuxt-link>
                         <!-- About Tab  -->
                        <nuxt-link to="/about"
                        class="text-gray-300 hover:bg-gray-700
                        hover:text-white px-3 py-2 rounded-md text-sm
                        font-medium"
                        >About</nuxt-link>
                        <nuxt-link to="/contact"
                        class="text-gray-300 hover:bg-gray-700
                        hover:text-white px-3 py-2 rounded-md text-sm
                        font-medium"
                        >Contact</nuxt-link>
                    </div>
                </div>
            </div>
        </div>
    </nav>
</template>
<style scoped>

</style>