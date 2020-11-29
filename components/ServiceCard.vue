<template>
  <a class="service-card" :href="service.url">
    <div class="service-card__icon">
      Icon
    </div>
    <div class="service-card__title">
      {{ service.title }}
    </div>
    <div class="service-card__description">
      {{ service.description }}
    </div>
<!--    <BaseButton>Подробнее</BaseButton>-->
  </a>
</template>

<script>
import BaseButton from '~/components/base/BaseButton.vue'

export default {
  components: {
    BaseButton
  },

  props: {
    service: Object
  }
}
</script>

<style lang="scss" scoped>
  .service-card {
    padding: 30px 18px;
    position: relative;
    background: #fff;
    text-align: center;
    transition: transform .2s;

    &:hover {
      transform: translateY(-5px);
    }

    &__icon {
      color: var(--accent-color);
      margin-bottom: 30px;
    }

    &__title {
      color: var(--primary-color);
      font-size: 24px;
      font-weight: 600;
      margin-bottom: 18px;
    }

    &__description {
      margin-bottom: 36px;
      color: #57667e;
      font-size: 16px;
    }
  }
</style>
