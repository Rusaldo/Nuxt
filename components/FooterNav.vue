<template>
  <nav class="footer-nav">
    <div class="footer-nav__block">
      <h3 class="footer-nav__title">О нас</h3>
      <ul class="footer-nav__list">
        <li class="footer-nav__item">
          <nuxt-link to="/services" class="footer-nav__link">Услуги</nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link to="/calculator" class="footer-nav__link">Калькулятор Калькулятор </nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link to="/calculator" class="footer-nav__link">Калькулятор</nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link to="/services" class="footer-nav__link">Услуги Услуги Услуги Услуги</nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link to="/calculator" class="footer-nav__link">Калькулятор</nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link to="/services" class="footer-nav__link">Услуги</nuxt-link>
        </li>
      </ul>
    </div>

    <div class="footer-nav__block">
      <h3 class="footer-nav__title">Сотрудничество</h3>
      <ul class="footer-nav__list">
        <li class="footer-nav__item">
          <nuxt-link to="/services" class="footer-nav__link">Услуги</nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link to="/calculator" class="footer-nav__link">Калькулятор Калькулятор </nuxt-link>
        </li>
        <li class="footer-nav__item">
          <nuxt-link to="/calculator" class="footer-nav__link">Калькулятор</nuxt-link>
        </li>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
  .footer-nav {
    display: flex;

     @include mobile {
       flex-direction: column;
     }

    &__block {
      &:not(:last-of-type) {
        margin-right: 48px;

        @include mobile {
          flex-direction: column;
          margin-right: 0;
          margin-bottom: 18px;
        }
      }
    }

    &__title {
      margin-bottom: 12px;
      font-weight: 500;
    }

    &__list {
      display: flex;
      flex-direction: column;
    }

    &__item {
      &:not(:last-child) {
        margin-bottom: 6px;
      }
    }

    &__link {
      &:hover {
        text-decoration: underline;
      }
    }
  }
</style>
