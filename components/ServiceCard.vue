<template>
  <article class="service-card">
    <h3 class="service-card__title">{{ service.title }}</h3>
    <BaseButton>Подробнее</BaseButton>
  </article>
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
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 0 10px 0 rgba(10,36,59,.27);
    min-height: 200px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    max-width: 480px;

    &__title {
      padding-top: 12px;
      margin-bottom: 18px;
    }
  }
</style>
