<template>
  <div class="flex justify-center gap-4 mb-4">
    <tabs-item :active="true" title="Рассылки" />
    <tabs-item title="Соцсети" />
    <tabs-item title="Мессенджеры" />
  </div>
</template>

<script setup>
import TabsItem from "./TabsItem.vue";
</script>

<style></style>
