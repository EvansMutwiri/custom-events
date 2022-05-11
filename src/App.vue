<script>
import PopUp from './components/PopUp.vue';
import FormVal from './components/FormVal.vue';

export default {
  components: {
    PopUp,
    FormVal,
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

  <body class="bg-lime-200 h-screen overflow-scroll">

    <FormVal>

      <template #title>
        <h1 class="bg-red-400 p-10 text-center text-2xl font-bold">Name slot: title</h1>
      </template>
      
      <p class="bg-red-400 p-10 text-center">This is a slot Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid impedit deleniti voluptates totam reiciendis. Nisi sit nam adipisci quis, eligendi unde iusto fugiat maxime repellat, perspiciatis quisquam voluptates amet. Ipsa!</p>
    <template #footer>
      <div class="flex bg-red-400 pb-6 text-sm">
        <p class="p-6 text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita, ratione.</p>
        <p class="p-6 text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet, assumenda.</p>
        <p class="p-6 text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet, assumenda.</p>
        <p class="p-6 text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet, assumenda.</p>
      </div>
    </template>
    
    </FormVal>
    <header>
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