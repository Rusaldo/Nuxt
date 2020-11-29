<template>
  <div class="footer-contacts">
    <address class="footer-contacts__contact">
      <a class="footer-contacts__link footer-contacts__link--phone" href="tel:+79253292121">+7 (925) 329-2121</a>
      <br>
      <a class="footer-contacts__link" href="mailto:brocker@brocker.ru">brocker@brocker.ru</a>
    </address>
    <address class="footer-contacts__contact">
      Офис на планете Земля: <br>
      Кремль, 1, Тверской район, Москва, 109012
    </address>
  </div>
</template>

<style lang="scss" scoped>
  .footer-contacts {
    &__contact {
      &:not(:last-of-type) {
        margin-bottom: 24px;
      }
    }

    &__link {
      transition: color .2s;

      &:hover {
        color: #fff;
      }

      &--phone {
        display: inline-block;
        font-size: 20px;
        color: #fff;
        margin-bottom: 6px;
      }
    }
  }
</style>
