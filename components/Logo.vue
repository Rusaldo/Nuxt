<template>
  <div class="logo">
    <nuxt-link to="/" class="logo__link">
      Broker<span class="logo__dot">.</span>
    </nuxt-link>
  </div>
</template>

<style lang="scss" scoped>
  .logo {
    display: flex;
    align-items: flex-end;

    &__link {
      font-size: 22px;
      font-weight: 500;
      color: var(--primary-color);
      text-transform: uppercase;
    }

    &__dot {
      line-height: 0;
      font-size: 35px;
    }
  }
</style>
