<template>
  <div>
    <nav class="nav">
      <div class="container">
        <h1>
          <nuxt-link to="/">Vue | Nuxt Js</nuxt-link>
        </h1>
        <ul>
          <li>
            <nuxt-link to="/">Home</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/posts">Posts</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/about">About</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/contact">Contact</nuxt-link>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>
<script>
export default {};

</script>
<style scoped>
.nav {
  position: relative;
  background-color: rgb(73, 126, 99);
  top: 0;
  left: 0;
  right: 0;
  transition: all 0.3s ease-in-out;
}


.nav .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 5px 0;
  transition: all 0.3s ease-in-out;
}

.nav ul {
  display: flex;
  list-style-type: none;
  align-items: center;
  justify-content: center;
  margin: 0px;
}

.nav a {
  color: #fff;
  text-decoration: none;
  padding: 7px 15px;
  transition: all 0.3s ease-in-out;
}

.nav.active {
  background-color: #fff;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
}

.nav.active a {
  color: #000;
}

.nav.active .container {
  padding: 10px 0;
}

.nav a.current,
.nav a:hover {
  color: #bbff00;
  font-weight: bold;
}

</style>