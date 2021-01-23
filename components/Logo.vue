<template>
  <nuxt-link class="logo" :class="{ 'logo--light': light }" to="/">
    <span style="color: var(--accent-color);">Базис</span>&nbsp;Кредит
  </nuxt-link>
</template>

<script>
export default {
  props: {
    light: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
  .logo {
    display: inline-flex;
    color: var(--secondary-color);
    font-size: 20px;
    font-weight: 400;
    text-transform: capitalize;

    @include tablet {
      font-size: 24px;
    }

    @include desktop {
      font-size: 30px;
    }

    /*&::after {*/
    /*  content: '';*/
    /*  width: 6px;*/
    /*  height: 6px;*/
    /*  border-radius: 30px;*/
    /*  background-color: var(--accent-color);*/
    /*  margin-top: auto;*/
    /*  margin-bottom: 6px;*/
    /*  margin-left: 2px;*/
    /*}*/

    &--light {
      color: #fff;
    }
  }
</style>
