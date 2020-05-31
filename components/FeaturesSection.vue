<template>
  <section class="section features">
    <div class="container">
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

<style lang="scss" scoped>
  .features {

    &__list {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-auto-rows: auto;
      gap: 24px;

      @include tablet {
        grid-template-columns: repeat(2, 1fr);
      }

      @include mobile {
        grid-template-columns: 100%;
      }
    }

    &__feature {
      text-align: center;
      font-size: 20px;

      @include mobile {
        font-size: 16px;
      }
    }

    &__icon {
      font-size: 40px;
      margin-bottom: 12px;

      @include mobile {
        font-size: 30px;
        margin-bottom: 6px;
      }
    }
  }
</style>
