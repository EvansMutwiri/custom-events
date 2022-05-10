<script>
import PopUp from './components/PopUp.vue';

export default {
  components: {
    PopUp
  },
  data() {
    return {
      name: '',
      isMenuOpen: false
    }
  },
  methods: {
    closePopUp(data) {
      this.isMenuOpen = false
      this.name = data
    }
  }
}

</script>

<template>

  <body class="bg-lime-400 h-screen">
    <header class="h-1/5">
    <p class="text-center font-bold text-xl">{{ name }}</p>
    </header>

    <div class="flex justify-center">
      <button class="bg-sky-200 p-4" @click="isMenuOpen = true">Show Alert</button>
    </div>

    <!-- v-if instead of v-show -->
    <pop-up v-if="isMenuOpen" @closePopUp="closePopUp"/>

  </body>

</template>

<style>
@import './assets/tailwind.css';
</style>