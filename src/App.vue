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
@import url('https://fonts.googleapis.com/css2?family=Righteous&display=swap');

* {
  font-family: 'Inter', sans-serif;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0.3);
}

.logo {
  font-family: 'Righteous', cursive;
}
</style>
