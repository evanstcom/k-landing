<template>
  <li class="breadcrumbs__item relative">
    <a
      href="#"
      class="text-neutral-400 hover:text-gray-700 filter transition duration-200 border-b border-blue-100 hover:border-blue-200"
    >
      {{ title }}</a
    >
  </li>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
a {
  font-size: 13px;
  padding-bottom: 2px;
}
.breadcrumbs__item::before {
  content: "→";
  position: absolute;
  font-size: 10px;
  top: 50%;
  transform: translateY(-50%);
  left: -28px;
  margin-right: 8px;
  margin-left: 8px;
  color: rgb(163 163 163);
}

.breadcrumbs__item:first-child::before {
  content: "";
}
</style>
