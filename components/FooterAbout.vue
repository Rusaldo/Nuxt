<template>
  <div class="footer-about">
    <Logo class="footer-about__logo" />
    <p class="footer-about__text">
      Кредитный, ипотечный брокер: помощь в получении кредита и ипотеки
    </p>
  </div>
</template>

<script>
  import Logo from '~/components/Logo.vue'

  export default {
    components: {
      Logo
    }
  }
</script>

<style lang="scss" scoped>
  .footer-about {

    &__logo {
      margin-bottom: 12px;
    }

    &__text {
      font-size: 14px;
    }
  }
</style>
