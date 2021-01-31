<template>
  <div class="success-page">
    <div class="section">
      <div class="container">
        <h2>Ваша заявка принята</h2>
        <p>В ближайшее время мы с вами свяжемся.</p>
        <nuxt-link class="success-page__back-link" to="/">← Вернуться назад</nuxt-link>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .success-page {
    font-size: 18px;
    text-align: center;
    min-height: 50vh;

    @include tablet {
      min-height: 60vh;
      font-size: 20px;
    }

    h2 {
      font-size: 24px;
      margin-bottom: 24px;

      @include tablet {
        font-size: 40px;
      }
    }

    &__back-link {
      display: inline-block;
      margin-top: 18px;
      color: var(--primary-color);
      transition: color .2s;

      &:hover {
        color: var(--accent-color)
      }
    }
  }
</style>
