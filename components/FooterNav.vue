<template>
  <nav class="footer-nav">
    <div class="footer-nav__block">
      <h3 class="footer-nav__heading">О нас</h3>
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
      <h3 class="footer-nav__heading">Сотрудничество</h3>
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
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
  .footer-nav {
    display: flex;

     @include tablet {
       justify-content: space-around;
     }

    @include tablet-max {
      flex-direction: column;
    }

    &__block {
      &:not(:last-of-type) {
        flex-direction: column;
        margin-right: 0;
        margin-bottom: 48px;

        @include tablet {
          margin-right: 48px;
          margin-bottom: 0;
        }
      }
    }

    &__heading {
      margin-bottom: 18px;
      color: #fff;
      font-size: 18px;
      font-weight: 500;
      text-transform: uppercase;

      @include tablet {
        margin-bottom: 36px;
      }
    }

    &__list {
      display: flex;
      flex-direction: column;
    }

    &__item {
      &:not(:last-child) {
        margin-bottom: 12px;
      }
    }

    &__link {
      display: block;
      transition: color .2s;

      &:hover {
        color: white;
      }
    }
  }
</style>
