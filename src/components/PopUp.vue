<template>
  <div class="text-white px-6 py-4 border-0 rounded relative mt-4 w-1/7 h-1/6 bg-lime-200">
      <span class="text-xl inline-block mr-5 align-middle">
        <i class="fas fa-bell" />
      </span>
      <span class="inline-block align-middle mr-8">
        <b class="capitalize">Pop up</b>!
      </span>
    </div>

    <div class="flex justify-center mt-4">
      <button class="bg-sky-200 mx-auto p-4" @click="$emit('closePopUp')">Close</button>
    </div>
</template>

<script setup>
  const emit = defineEmits('closePopUp')
</script>

<style>

</style>