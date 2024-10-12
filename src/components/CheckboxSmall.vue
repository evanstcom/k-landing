<template>
  <div class="flex gap-2 items-center">
    <label class="flex items-center gap-2 cursor-pointer">
      <div
        class="w-8 h-4 rounded-full"
        :class="isSubscribe ? 'bg-blue-500' : ' bg-slate-300'"
      >
        <div
          class="w-4 h-4 rounded-full bg-white border transition-all duration-200"
          :class="isSubscribe ? 'ml-4 border-blue-500' : 'border-slate-300 '"
        ></div>
      </div>
      <input
        class="absolute w-0 h-0 opacity-0 -z-20"
        type="checkbox"
        @click="toSubscribe"
      />
    </label>
    <span class="text-sm pt-1">Подписаться на все рассылки</span>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isSubscribe = ref(false);

function toSubscribe(e) {
  isSubscribe.value = e.target.checked;
}
</script>

<style></style>
