<template>
  <section>
    <card>
      <div class="greeting">
        <div class="greeting__logo">
          <img src="@/assets/icons/date.svg" alt="title" />
        </div>
        <div class="greeting__marquee">
          <scroll-marquee text="Приглашение" />
        </div>
        <div class="greeting__image">
          <picture>
            <source srcset="@/assets/images/newlyweds.webp" type="image/webp">
            <img src="@/assets/images/newlyweds.jpg" alt="молодожены" />
          </picture>
        </div>
        <div class="greeting__content">
          <h1 v-animate.title class="title _anim-title">
            ДОРОГИЕ НАШИ РОДСТВЕННИКИ И ДРУЗЬЯ
          </h1>
          <p v-animate class="text _anim-text">
            Этим летом мы устраиваем особенный праздник — уютную свадебную вечеринку под открытым небом.
          </p>
          <p v-animate class="text _anim-text">
            Этот день мы мечтаем разделить с вами — нашими родными и близкими.
            Будет тепло, по-домашнему, с любовью и танцами.
          </p>
        </div>
      </div>
    </card>
  </section>
</template>

<script setup>
import Card from '@/components/atom/card/index.vue'
import ScrollMarquee from '@/components/atom/marquee/index.vue'
</script>

<style scoped lang="scss">
.greeting {
  display: flex;
  flex-direction: column;
  gap: 30px;

  &__marquee {
    position: absolute;
    padding: 5px 0;
    width: 100%;
    top: 100px;
    left: 0;
    background-color: #fff;
    border-top: 1.5px solid #000;
    border-bottom: 1.5px solid #000;
  }

  &__image {
    margin-top: 50px;
    width: 100%;
    height: 400px;
    position: relative;

    img {
      border-radius: 50% 50% 0 0;
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      object-fit: cover;
      object-position: 0 8%;
    }
  }

  &__content {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .title {
    transition-delay: 0.2s;
  }

  p {
    &:nth-of-type(1) {
      transition-delay: 0.3s;
    }
    &:nth-of-type(2) {
      transition-delay: 0.4s;
    }
  }

}
</style>
