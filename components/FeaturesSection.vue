<template>
  <section class="section features">
    <div class="container">
      <SectionTitle>Наши преимущества</SectionTitle>
      <ul class="features__list">
        <li class="features__feature">
          <div class="features__icon">📉</div>
          Снижаем процентную ставку через банки-партнеры
        </li>
        <li class="features__feature">
          <div class="features__icon">🕐</div>
          Экономим ваше время, деньги и нервы
        </li>
        <li class="features__feature">
          <div class="features__icon">🔒</div>
          Оплата по факту выдачи кредита
        </li>
        <li class="features__feature">
          <div class="features__icon">🏢</div>
          Офисы рядом с метро
        </li>
        <li class="features__feature">
          <div class="features__icon">😎</div>
          Квалифицированные сотрудники
        </li>
        <li class="features__feature">
          <div class="features__icon">📜</div>
          Мы — сертифицированная компания
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import SectionTitle from '~/components/SectionTitle.vue'

export default {
  components: {
    SectionTitle
  }
}
</script>

<style lang="scss" scoped>
  .features {

    &__list {
      grid-template-columns: 100%;
      display: grid;
      grid-auto-rows: auto;
      gap: 24px;

      @include tablet {
        grid-template-columns: repeat(2, 1fr);
      }

      @include desktop {
        grid-template-columns: repeat(3, 1fr);
      }
    }

    &__feature {
      text-align: center;
      font-size: 16px;

      @include tablet {
        font-size: 20px;
      }
    }

    &__icon {
      font-size: 30px;
      margin-bottom: 6px;

      @include tablet {
        font-size: 40px;
        margin-bottom: 12px;
      }
    }
  }
</style>
