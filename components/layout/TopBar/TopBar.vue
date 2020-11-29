<template>
  <div class="top-bar">
    <div class="container top-bar__container">
      <div class="top-bar__contacts">
        <a class="top-bar__link" href="">+7 999 999 0000 </a>
        <span>Пн–Пт 10:00–19:00</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {
  }
}
</script>

<style lang="scss" scoped>
  .top-bar {
    background-color: #0d2d3e;
    color: #fff;
    padding: 12px 0;
    font-weight: 500;
    z-index: 10;

    &__container {
      display: flex;
      justify-content: center;

      @include tablet {
        justify-content: flex-end;
      }
    }

    &__link {
      transition: color .2s;

      &:hover {
        color: var(--accent-color)
      }

      &:not(:last-child) {
        margin-right: 18px;
      }
    }
  }
</style>
