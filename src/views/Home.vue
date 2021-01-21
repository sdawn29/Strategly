<template>
  <div class="home">
    <div class="mb-4 tracking-widest text-sm font-light">
      ASSETO CORSA COMPITIZIONE
    </div>
    <div class="grid grid-cols-2 gap-4">
      <div class="bg-gradient-to-r from-teal-400 to-blue-500 hover:from-blue-400 hover:to-teal-500 p-4 rounded-lg font-semibold cursor-pointer text-white text-center" @click="$router.push({name: 'Fuel'})">
        Fuel Calculator
      </div>
      <!-- <div class="bg-gradient-to-r from-purple-400  to-red-500 hover:from-red-400 hover:to-purple-500 p-4 font-semibold rounded-lg cursor-pointer text-white text-center">
        Strategy
      </div>
      <div class="bg-gradient-to-r from-green-500 to-blue-400 hover:from-blue-500 hover:to-green-400 p-4 font-semibold rounded-lg cursor-pointer text-white text-center">
        Car Setup
      </div> -->
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
}
}
</script>
