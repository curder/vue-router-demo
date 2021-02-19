<template>
  <div id="nav">
    <p class="logo">Travel App</p>
    <ul class="nav-links">
      <li class="links">
        <router-link :to="{ name: 'home' }">Home</router-link>
      </li>
      <li
        v-for="destination in destinations"
        :key="destination.name"
        class="links"
      >
        <router-link
          :to="{
            name: 'destinationDetails',
            params: { slug: destination.slug }
          }"
          v-text="destination.name"
        ></router-link>
      </li>
      <li class="links">
        <router-link :to="{ name: 'user' }">Dashboard</router-link>
      </li>
    </ul>
  </div>
</template>
<script>
import store from "@/store";

export default {
  data() {
    return {
      destinations: store.destinations
    };
  }
};
</script>
<style scoped>
#nav {
  display: flex;
  align-items: center;
  position: sticky;
  top: 0;
  background-color: white;
  border-bottom: 1px solid #eaeaea;
  z-index: 1;
}

#nav a {
  color: #2c3e50;
  text-decoration: none;
  font-weight: bold;
}

#nav a.exact-active-class {
  color: #ab26ab;
}

.nav-links {
  display: flex;
}

.links {
  padding-right: 20px;
  list-style: none;
}

.links:hover {
  text-decoration: underline;
}

.logo {
  font-size: 20px;
  color: purple;
  font-weight: bold;
}
</style>
