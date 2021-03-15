<template>
  <div>
      <Navbar/>
    <div class="container mt-5">
      <div class="row">
        <div class="col-12 justify-content-center d-flex mb-5 p-relative">
          <button type="button" class="back-btn shadow">
            <nuxt-link to="posts">Back to Posts</nuxt-link>
          </button>
          <img :src="post.image" class="post-img" alt="" />
        </div>
        <div class="col-12">
          <h3 class="border-bottom pb-2 mb-3 bold text-center">
            {{ post.title }}
          </h3>
          <div class="d-flex">
            <h5>Height : {{ post.height }}</h5>
          </div>
          <div class="d-flex">
            <h5>
              Countries :
              <span v-for="country in post.countries" :key="country">{{
                country
              }}</span>
            </h5>
          </div>
          <p>{{ post.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

import Navbar from '@/components/Navbar.vue'
export default {
    components : {
        Navbar
    },
    async asyncData({ params, $axios }) {
        const post = await $axios.$get(
        `https://api.nuxtjs.dev/mountains/${params.post}`
        );
        console.log(post);
        return { post };
    },
};
</script>
<style scoped>
.post-img {
  width: 500px;
  height: 300px;
  border-radius: 10px;
  object-fit: cover;
}

.back-btn {
  position: absolute;
  top: 50px;
  left: 50px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
.back-btn a {
  color: #000;
  padding: 10px 50px;
}
</style>