<template>
  <div class="w-full bg-white px-4 py-6 rounded-xl drop-shadow-md">
    <div class="flex justify-between mb-2 md:gap-6">
      <div class="flex flex-col justify-between gap-1">
        <span class="text-sm text text-neutral-400">{{ card.subtitle }}</span>
        <h3 class="font-semibold text-xl -mt-1">{{ card.title }}</h3>
        <p class="text-sm mb-4 text-neutral-500 hidden md:block mt-2">
          {{ card.text }}
        </p>
      </div>
      <div class="w-10 md:min-w-20 md:h-20">
        <img class="w-full" :src="card.image" :alt="card.title" />
      </div>
    </div>
    <p class="text-sm mb-4 text-neutral-500 md:hidden">
      {{ card.text }}
    </p>
    <div class="flex flex-col gap-2 mb-6">
      <div v-for="tab in card.tabs" :key="tab" class="flex items-center gap-2">
        <img class="w-4 h-4" src="/check.svg" alt="" />
        <span class="text-sm">{{ tab }}</span>
      </div>
    </div>
    <Checkbox :value="card.checkbox" :label="card.checkboxText" />
  </div>
</template>

<script setup>
import Checkbox from "./Checkbox.vue";
defineProps({
  card: {
    type: Object,
  },
});
</script>

<style></style>
