<template>
   <div>
        <Navbar/>
        <div class="custom-container shadow">
            <div class="row m-5">
            <h1 class="border-bottom mb-3 pb-2 text-center">Mountains</h1>
            </div>
            <div class="inner-container">
            <div class="row bg-white p-3 mb-5">
                <Post v-for="post in posts" :key="post" :post="post" />
            </div>
            </div>
        </div>
   </div>
  
</template>


<script>
import Post from "@/components/Post.vue";
import Navbar from '@/components/Navbar.vue' 

export default {
  components: {
    Post,
    Navbar
  },
  data() {
    return {
      posts: [],
    };
  },
  async fetch() {
    this.posts = await fetch("https://api.nuxtjs.dev/mountains").then((res) =>
      res.json()
    );
  },
};
</script>


<style scoped>
</style>