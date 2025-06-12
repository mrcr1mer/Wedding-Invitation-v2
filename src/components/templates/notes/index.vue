<template>
  <section class="notes">
    <div class="notes__date">
      <h2 v-animate.title class="date-title title">До свадьбы осталось</h2>
      <countdown-timer v-animate target-date="2025-07-19" />
    </div>
  </section>
</template>

<script setup>
import CountdownTimer from "@/components/atom/countdown-timer/index.vue"
import Card from "@/components/atom/card/index.vue"
</script>

<style lang="scss" scoped>
.notes {

  .date-title {
    text-align: center;
    margin-bottom: 20px;
  }

  .card {
    text-align: left;
  }

  &__title {
    margin-bottom: 20px;

    @media (max-width: 375px) {
      @supports (hyphens: auto) {
        hyphens: auto;
      }

      @supports not(hyphens: auto) {
        word-break: break-word;
      }
    }
  }

  .text {
    &:not(:last-child) {
      margin-bottom: 20px;
    }
  }
}
</style>
