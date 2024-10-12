<script setup>
import Header from "./components/Header.vue";
import BreadcrumbsList from "./components/BreadcrumbsList.vue";
import TabsList from "./components/TabsList.vue";
import FormSubscribe from "./components/FormSubscribe.vue";
import CardList from "./components/CardList.vue";
</script>

<template>
  <Header />
  <BreadcrumbsList />
  <h1
    class="text-center text-3xl font-semibold mt-2 mb-6 lg:text-5xl tracking-wide lg:mt-8 lg:mb-10"
  >
    Подписки «Клерка»
  </h1>
  <TabsList />
  <section>
    <div
      class="info-container px-4 py-8 bg-gray-100 lg:container lg:mx-auto lg:px-6 lg:py-12 lg:rounded-lg"
    >
      <h2 class="text-2xl font-semibold mb-4 lg:mb-6 lg:text-center">
        Выберите рассылки, которые подходят именно вам
      </h2>
      <FormSubscribe />
      <CardList />
    </div>
  </section>
  <div class="flex justify-center my-12">
    <img class="text-center" src="/smile.svg" alt="" />
  </div>
</template>

<style scoped>
.info-container {
  margin-top: -2px;
}
</style>
