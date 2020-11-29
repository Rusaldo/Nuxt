<template>
  <div class="navbar">
    <button class="navbar__burger" :class="{ 'active': isMenuVisible }" @click="toggleMenu">&#9776;</button>
    <transition name="slide">
      <nav class="navbar__links" :class="{ 'hidden': !isMenuVisible }">
        <nuxt-link to="/services" class="navbar__link">Услуги</nuxt-link>
        <nuxt-link to="/calculator" class="navbar__link">Кредитный калькулятор</nuxt-link>
        <nuxt-link to="/about" class="navbar__link">О нас</nuxt-link>
      </nav>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuVisible: false
    }
  },

  methods: {
    toggleMenu() {
      this.isMenuVisible = !this.isMenuVisible
    }
  }
}
</script>

<style lang="scss" scoped>
  .navbar {

    &__burger {
      background: transparent;
      border: none;
      color: #000;
      outline: none;
      font-size: 26px;
      line-height: 1;
      padding: 18px;
      margin-right: -12px;

      @include tablet {
        display: none;
      }

      &.active {
        color: var(--accent-color);
      }
    }

    &__links {
      font-size: 18px;
      display: flex;

      @include tablet-max {
        position: absolute;
        top: 100%;
        left: 0;
        right: 0;
        width: 100%;
        background-color: #fff;
        flex-direction: column;
        border-top: 1px solid #cfcfcf;
        box-shadow: 0 10px 15px rgba(25, 25, 25, 0.1);
        text-align: center;
      }

      &.hidden {
        @include tablet-max {
          display: none;
        }
      }
    }

    &__link {
      padding: 12px;
      display: block;
      white-space: nowrap;
      transition: color .2s;
      color: var(--secondary-color);

      &:hover,
      &.nuxt-link-exact-active {
        color: var(--accent-color);
      }

      @include tablet {
        padding: 30px 18px;
      }
    }
  }
</style>
