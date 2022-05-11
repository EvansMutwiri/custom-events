<template>
  <slot name="title"></slot>
  <slot></slot>
  <slot name="footer"></slot>
  <div class="center-btn">
    <button class="p-2 bg-sky-400" :class=" active ? 'text-green' : 'text-red'" @click="toggle">Click me</button>
  </div>
  
  
</template>

<script>
import { ref } from '@vue/reactivity';
export default {
  methods: {
    toggle () {
      this.active = !this.active;
    }
  },
  
  data() {

    return {
      active : ref(true)
    }
  }
}
</script>

<style scoped>
  .center-btn {
    height: 100vh;
    display: grid;
    place-items: center;
    overflow: scroll;
  }

  .text-red {
    color: white;
    background: red;
  }

  .text-green{
    color: green;
  }
</style>