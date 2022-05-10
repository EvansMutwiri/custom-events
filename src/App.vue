<script setup>
import { ref } from 'vue';
import PopUp from './components/PopUp.vue';

// export default {
  // components: {
  //   PopUp
  // },
  // data() {
  //   return {
  //     isMenuOpen: false
  //   }
  // }
  
// }

//using setup method

const isMenuOpen = ref(false);

</script>

<template>

  <body class="bg-lime-400 h-screen">
    <header class="h-1/5">

    </header>

    <div class="flex justify-center">
      <button class="bg-sky-200 p-4" @click="isMenuOpen = true">Show Alert</button>
    </div>

    <!-- v-if instead of v-show -->
    <pop-up v-if="isMenuOpen" @closePopUp="isMenuOpen = false"/>

  </body>

</template>

<style>
@import './assets/tailwind.css';
</style>