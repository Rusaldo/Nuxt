<template>
  <nuxt-link class="logo" :class="{ 'logo--light': light }" to="/">
    Базис Кредит
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
    font-size: 18px;
    font-weight: 500;
    text-transform: capitalize;

    @include tablet {
      font-size: 22px;
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
