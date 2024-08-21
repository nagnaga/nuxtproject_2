<script setup>
// Fetch all post
const {data,error,pending} = useLazyFetch("https://dummyjson.com/posts?limit=10");
console.log(data);
useHead({
    title:"Home",
    })

</script>

<template>
    <div v-if="error" class="text-2xl text-white">an error occured.....{{ error }}</div>
    <div v-else-if="data">
        <div class v-for="{id,title,body} in data.posts" :key="id">
            <postcard :id="id" :title="title":body="body" />
            <!-- props sending -->
        </div>
    </div>
    <div v-else class="text-2xl text-white">Loading....</div>
</template>


<style  scoped>

</style>
<!-- <div v-for="n in 8">
<postcard/>
</div> -->