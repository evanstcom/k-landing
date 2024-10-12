<template>
  <div class="mt-6 flex flex-col gap-4 lg:grid lg:grid-cols-2">
    <CardListItem v-for="card in cards" :key="card.title" :card="card" />
  </div>
</template>

<script setup>
import CardListItem from "./CardListItem.vue";

const cards = [
  {
    subtitle: "Перед рассветом",
    title: "Утренний бухгалтер",
    text: "Самые важные новости и события за день. Кратко, по делу, структурировано.",
    image: "./card-1.png",
    tabs: [
      "Новости для бухгалтеров, ИП и директора",
      "Подборка статей за день",
    ],
    checkboxText: "Уже получают 59 342 человек",
    checkbox: true,
  },
  {
    subtitle: "После заката",
    title: "Ночной бухгалтер",
    text: "Самая краткая газета о налогах и бухучете в мире — современная рассылка для чтения.",
    image: "./card-2.png",
    tabs: [
      "Анализ, оценка и только самое главное",
      "Лучшие комменты юзеров в обзоре",
    ],
    checkboxText: "Уже получает 37 480 человек",
    checkbox: false,
  },
  {
    subtitle: "Раз в две недели",
    title: "Ножницы скидок",
    text: "Подборка самых выгодных и полезных спецпредложений от надежных компаний.",
    image: "./card-3.png",
    tabs: [
      "Акции и скидки от лидеров рынка",
      "Те, кто подписался – экономят много денег ",
    ],
    checkboxText: "Уже получает 92 118 человек",
    checkbox: false,
  },
  {
    subtitle: "По мере появления анонсов",
    title: "Чемодан вебинаров",
    text: "Подборка с анонсами бесплатных вебинаров на самые топовые темы при участии экспертов.",
    image: "./card-4.png",
    tabs: [
      "Никогда не пришлем платные вебинары",
      "Подборка топовых тем для вебинаров",
    ],
    checkboxText: "Уже получает 92 082 человек",
    checkbox: false,
  },
];
</script>

<style></style>
