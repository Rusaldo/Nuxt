<template>
  <header class="header">
    <div class="container header__container">
      <Logo class="header__logo" />
<!--      <NavBar class="header__navbar" />-->
      <div class="header__contacts">
        <a class="header__contact header__contact--phone" href="tel:+74951350666">+7 (495) 135 0666</a>
        <a class="header__contact header__contact--email" href="mailto:contact@basiscredit.info">contact@basiscredit.info</a>
      </div>
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
    background-color: white;

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

  .header__contacts {
    display: flex;
    flex-direction: column;
    text-align: right;
  }

  .header__contact {
    font-size: 16px;
    color: var(--primary-color);
    transition: color .2s;

    @include tablet {
      font-size: 20px;
    }

    &:hover {
      color: var(--accent-color);
    }

    &:active {
      color: var(--accent-color);
    }

    &--phone {
      font-weight: 500;
    }

    &--email {
      font-size: 14px;
      margin-top: 2px;

      @include tablet {
        font-size: 16px;
      }
    }
  }
</style>
