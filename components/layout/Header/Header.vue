<template>
  <header class="header">
    <div class="container header__container">
      <Logo class="header__logo" />
<!--      <NavBar class="header__navbar" />-->
      <a class="header__phone" href="tel:79999990000">+7 999 999 0000</a>
    </div>
  </header>
</template>

<script>
import Logo from '~/components/Logo.vue'
import NavBar from '~/components/NavBar.vue'

export default {
  components: {
    Logo,
    NavBar
  }
}
</script>

<style lang="scss" scoped>
  .header {
    box-shadow: 0 10px 15px rgba(25, 25, 25, 0.1);
    position: relative;
    z-index: 10;
    height: 61px;

    @include tablet {
      height: 84px;
    }
  }

  .header__container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100%;
  }

  .header__phone {
    font-weight: 500;
    font-size: 20px;
    color: var(--primary-color);
  }
</style>
