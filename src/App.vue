<template>
  <div class="md:w-1/3 md:mx-auto px-4">
    <Navbar/>
    <router-view/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');

* {
  font-family: 'Inter', sans-serif;
  user-select: none; /* standerd */
  -moz-user-select: none; /* firefox specific */
  -webkit-user-select: none; /* Chrome, Opera and Safari*/
  -ms-user-select: none; /* IE, ms-edge */
}
</style>
