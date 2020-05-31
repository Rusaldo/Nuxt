<template>
  <nav class="navbar">
    <nuxt-link to="/services" class="navbar__link">Услуги</nuxt-link>
    <nuxt-link to="/calculator" class="navbar__link">Кредитный калькулятор</nuxt-link>
    <nuxt-link to="/about" class="navbar__link">О нас</nuxt-link>
  </nav>
</template>

<style lang="scss" scoped>
  .navbar {
    font-size: 18px;

    @include mobile {
      display: flex;
      flex-wrap: wrap;
    }

    &__link {
      white-space: nowrap;
      transition: color .2s;

      &:hover,
      &.nuxt-link-exact-active {
        color: var(--primary-color);
      }

      &:not(:last-of-type) {
        margin-right: 24px;
      }
    }
  }
</style>
