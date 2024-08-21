<script setup>
definePageMeta({
  layout:'custom',
})
const route = useRoute()
// Fetch single post
const {data :post,error,pending} = useLazyFetch(`https://dummyjson.com/posts/${route.params.id}`);
// here v changed name of the data to post . now data will be called as post.
console.log(post);
useHead({
    title:"Post detail",
    })


</script>

<template>
 <div>
  <div v-if="error" class="text-2xl text-white">an error occured.....{{ error }} </div>
  <div v-else-if="data">
    <PostDetail :id="post.id" :title="post.title" :body="post.body" />
  </div> 
 <div v-else class="text-2xl text-white"> Loading....</div>
</div>
</template>

<style  scoped>

</style>