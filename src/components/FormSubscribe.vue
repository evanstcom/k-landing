<template>
  <form action="">
    <div class="relative mb-4">
      <input
        class="p-4 w-full outline-none"
        type="text"
        placeholder="Электронная почта"
      />
      <button
        type="submit"
        class="lg:hidden bg-blue-500 rounded-full h-14 w-14 flex items-center justify-center absolute top-0 right-0 hover:bg-blue-400 transition-colors duration-200"
      >
        <img src="/submit.svg" alt="" />
      </button>
      <button
        type="submit"
        class="hidden lg:block bg-blue-500 rounded-full h-14 w-40 text-white items-center justify-center absolute top-0 right-0 hover:bg-blue-400 transition-colors duration-200"
      >
        Подписаться
      </button>
    </div>
    <Checkbox />
  </form>
</template>

<script setup>
import Checkbox from "./CheckboxSmall.vue";
</script>

<style scoped>
input {
  border-top-left-radius: 6px;
  border-bottom-left-radius: 6px;
  border-top-right-radius: 27px;
  border-bottom-right-radius: 27px;
}
</style>
