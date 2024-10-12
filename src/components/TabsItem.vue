<template>
  <li>
    <a
      :class="
        active
          ? 'text-4 text-blue-500 font-medium px-2 pb-4 border-b-2 border-blue-500'
          : 'text-4 text-gray-600 px-2 hover:text-blue-500 transition-colors duration-200'
      "
      href="#"
    >
      {{ title }}
    </a>
  </li>
</template>

<script setup>
defineProps({
  active: {
    type: Boolean,
    default: false,
  },
  title: {
    type: String,
    required: true,
  },
});
</script>

<style>
li {
  list-style-type: none;
}
</style>
