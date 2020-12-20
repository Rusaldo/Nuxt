<template>
  <h2 class="section-title" :class="{ 'section-title--center': center }">
    <slot />
  </h2>
</template>

<script>
export default {
  props: {
    center: Boolean
  }
}
</script>

<style lang="scss" scoped>
  .section-title {
    font-size: 28px;
    font-weight: 700;
    margin-bottom: 40px;
    color: #092c3f;
    position: relative;
    text-align: center;
    padding-bottom: 18px;

    @include tablet {
      margin-bottom: 50px;

      &:not(.section-title--center) {
        text-align: left;
        padding-left: 68px;
        padding-bottom: 0;
      }
    }

    &::before {
      content: '';
      position: absolute;
      width: 54px;
      height: 2px;
      background: var(--accent-color);
      left: 50%;
      bottom: 0;
      transform: translateX(-50%);
    }

    @include tablet {
      &:not(.section-title--center):before {
        left: 0;
        top: 50%;
        transform: translateY(-50%);
      }
    }

    @include tablet {
      font-size: 40px;
      margin-bottom: 70px;
    }
  }
</style>
