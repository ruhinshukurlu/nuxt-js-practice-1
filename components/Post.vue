<template>
  <div class="post-item mb-5">
    <nuxt-link :to="post.slug">
      <div class="row">
        <div class="col-3">
          <img :src="post.image" alt="" />
        </div>
        <div class="col-8">
          <div class="d-column">
            <h3 class="border-bottom pb-2 mb-3">{{ post.title }}</h3>

            <p>{{ post.description }}</p>
            <div class="d-flex">
              <span>Countries : </span>
              <ul class="d-flex country-list">
                <li
                  v-for="country in post.countries"
                  :key="country"
                  class="mr-1"
                >
                  {{ country }},
                </li>
              </ul>
            </div>

            <div class="d-flex">
                <span>Height : </span>
                <span> {{post.height}}</span>
            </div>
          </div>
        </div>
      </div>
    </nuxt-link>
  </div>
</template>
<script>

export default {
    props: ["post"],
};
</script>
<style scoped>
.post-item img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  border-radius: 10px;
}
.country-list {
  margin: 0px;
  padding: 0px;
}

.country-list li {
  margin-right: 5px;
}

.post-item a{
    text-decoration: none;
    color: #000;
}

.post-item{
    transition: ease-in-out .3s;
    padding: 10px;
}

.post-item:hover{
    transform: scale(1.02);
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.35)!important;
}
</style>