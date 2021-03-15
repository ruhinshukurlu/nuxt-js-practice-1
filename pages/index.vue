<template>
  <div>
    <Navbar/> 
    <div  class="container mt-5 pt-5 d-column">
      
      <Logo />
      <h1 class="title">nuxt-practice-1</h1>
      <div class="links">
        <h3>
          Working on Dynamic Routing, Fetching data from API, Componenets | Props  
        </h3>
        <a
          href="https://github.com/ruhinshukurlu/nuxt-js-practice-1"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Github Repostory for This Project
        </a>

      </div>
    </div>
  </div>
</template>

<script>

import Navbar from '@/components/Navbar.vue'

export default {
  components : {
    Navbar
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}



</style>
