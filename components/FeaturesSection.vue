<template>
  <section class="section features">
    <div class="container">
      <SectionTitle>Наши преимущества</SectionTitle>
      <ul class="features__list">
        <li class="features__feature">
          <IconPartners class="features__icon" />
          <h4 class="features__heading">Скорость</h4>
          <p class="features__description">Предоставим решение по кредиту за 1 день с минимальным пакетом документов</p>
        </li>
        <li class="features__feature">
          <IconContract class="features__icon" />
          <h4 class="features__heading">Выгодные условия</h4>
          <p class="features__description">Подберем для вас самое выгодное предложение на рынке среди более чем 50 банков партнеров</p>
        </li>
        <li class="features__feature">
          <IconPartners class="features__icon" />
          <h4 class="features__heading">Удобство</h4>
          <p class="features__description">Мы предоставляем возможность провести сделку онлайн, что сэкономит вам время и деньги</p>
        </li>
        <li class="features__feature">
          <IconPartners class="features__icon" />
          <h4 class="features__heading">Профессионализм</h4>
          <p class="features__description">Все наши специалисты имеют опыт работы от 3 лет в банковской сфере и являются профессионалами в своих областях</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import SectionTitle from '~/components/SectionTitle.vue'
import IconBanknote from '~/components/icons/IconBanknote'
import IconPartners from '~/components/icons/IconPartners'
import IconContract from '~/components/icons/IconContract'

export default {
  components: {
    SectionTitle,
    IconBanknote,
    IconPartners,
    IconContract
  }
}
</script>

<style lang="scss" scoped>
  .features {

    &__list {
      grid-template-columns: 100%;
      display: grid;
      grid-auto-rows: auto;
      gap: 60px 30px;

      @include tablet {
        gap: 60px;
      }

      @include laptop {
        grid-template-columns: repeat(2, 1fr);
        gap: 90px 60px;
      }
    }

    &__feature {
      display: grid;
      grid-template-columns: auto auto;
      grid-auto-rows: auto;
      column-gap: 24px;

      @include laptop {
        column-gap: 30px;
      }
    }

    &__icon {
      width: 42px;
      height: 42px;
      font-size: 30px;
      margin-bottom: 6px;
      grid-row: 1 / 3;
      color: var(--primary-color);
      margin-top: 6px;

      @include tablet {
        font-size: 40px;
        margin-bottom: 12px;
      }

      @include laptop {
        width: 72px;
        height: 72px;
      }
    }

    &__heading {
      font-size: 18px;
      font-weight: 500;
      margin-bottom: 6px;
      color: var(--primary-color);

      @include tablet {
        font-size: 24px;
      }
    }

    &__description {
      grid-column: 2 / 3;
      font-size: 16px;

      @include tablet {
        font-size: 20px;
      }
    }
  }
</style>
