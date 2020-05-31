<template>
  <div class="footer-contacts">
    <address class="footer-contacts__contact">
      Офис на планете Земля: <br>
      Кремль, 1, Тверской район, Москва, 109012
    </address>
    <address class="footer-contacts__contact">
      +7 (999) 999-9999 <br>
      brocker@brocker.ru
    </address>
  </div>
</template>

<style lang="scss" scoped>
  .footer-contacts {
    color: var(--text-gray-color);
    font-size: 14px;

    &__contact {
      &:not(:last-of-type) {
        margin-bottom: 24px;
      }
    }
  }
</style>
