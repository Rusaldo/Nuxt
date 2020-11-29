<template>
  <h3 class="section-title">
    <slot />
  </h3>
</template>

<style lang="scss" scoped>
  .section-title {
    font-size: 30px;
    font-weight: 700;
    margin-bottom: 50px;
    color: #092c3f;
    position: relative;
    padding-left: 68px;

    &::before {
      content: '';
      position: absolute;
      width: 54px;
      height: 2px;
      background: var(--accent-color);
      left: 0;
      top: 50%;
      transform: translateY(-50%);
    }

    @include tablet {
      font-size: 40px;
      margin-bottom: 70px;
    }
  }
</style>
