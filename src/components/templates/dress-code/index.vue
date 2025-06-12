<template>
  <section class="dress-code">
    <h2 v-animate.title class="title">дресс-код</h2>
    <p v-animate class="text">
      <span>Девушки: </span> — лёгкое платье.
    </p>
    <p v-animate class="text">
      <span>Мужчины: </span> — рубашка и брюки.
    </p>
    <p v-animate class="text"><span>❗Обратите внимание: </span> мероприятие будет проходить на траве, поэтому просим девушек быть без каблуков — пусть будет красиво и удобно!<span></span></p>
  </section>
</template>

<script setup>
import AcceptableColors from "@/components/atom/acceptable-colors/index.vue"

const womanColors = [
  {
    color: "#ffd1ba",
    label: "Персиковый"
  },
  {
    color: "#b8defb",
    label: "Голубой"
  },
  {
    color: "#a4ac7d",
    label: "Фисташковый"
  }
]

const manColors = [
  {
    color: "#000",
    label: "Черный"
  },
  {
    color: "#01013f",
    label: "Синий"
  },
  {
    color: "#c4a996",
    label: "Бежевый"
  },
  {
    color: "#a8a5ac",
    label: "Серый"
  }
]

</script>

<style lang="scss" scoped>
.dress-code {
  display: flex;
  flex-direction: column;
  gap: 20px;
  background-color: #3c3f35;
  color: #fff;

  &__colors-label {
    margin-bottom: 10px;
    font-weight: 500;
  }
}
</style>
