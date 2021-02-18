<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
    <router-link :to="{ name: 'brazil' }">Brazil</router-link>
    <router-link :to="{ name: 'hawaii' }">Hawaii</router-link>
    <router-link :to="{ name: 'jamaica' }">Jamaica</router-link>
    <router-link :to="{ name: 'panama' }">Panama</router-link>
  </div>
</template>
<script>
export default {
  //
}
</script>
