<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__top-container">
        <div class="footer__about">
          <Logo class="footer__logo" light />
          <p>
            Кредитный, ипотечный брокер: помощь в получении кредита и ипотеки
          </p>
        </div>
<!--        <FooterNav />-->
        <div class="footer__contacts">
          <address class="footer__contact">
            <a class="footer__contact-link footer__contact-link--phone" href="tel:+79253292121">+7 (925) 329-2121</a>
            <br>
            <a class="footer__contact-link" href="mailto:brocker@brocker.ru">brocker@brocker.ru</a>
          </address>
          <address class="footer__contact">
            Офис на планете Земля: <br>
            Кремль, 1, Тверской район, Москва, 109012
          </address>
        </div>
      </div>
      <div class="footer__bottom">
        <p>
          © ИП «Русалдо» 1997-2020. Кредитный и ипотечный брокер: помощь в получении кредита и ипотеки
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
  import Logo from '~/components/Logo.vue'
  import FooterAbout from '~/components/FooterAbout.vue'
  import FooterNav from '~/components/FooterNav.vue'
  import FooterContacts from '~/components/FooterContacts.vue'
  import FooterBottom from '~/components/FooterBottom.vue'

  export default {
    components: {
      Logo,
      FooterAbout,
      FooterNav,
      FooterContacts,
      FooterBottom
    }
  }
</script>

<style lang="scss" scoped>
 .footer {
   background-color: #11141b;
   color: #bdbdbd;

   &__top-container {
     display: grid;
     gap: 48px;
     grid-template-columns: 100%;
     padding-top: 30px;
     padding-bottom: 30px;

     @include tablet {
       grid-template-columns: 250px 1fr;
       grid-auto-rows: auto;
       padding-top: 100px;
       padding-bottom: 100px;
     }

     @include desktop {
       padding-top: 120px;
       grid-template-columns: 250px 1fr auto;
       gap: 60px;
     }
   }

   &__logo {
     margin-bottom: 18px;

     @include tablet {
       margin-bottom: 30px;
     }
   }

   &__contacts {
     @include tablet {
       grid-column: 1 / 3;
     }

     @include desktop {
       grid-column: unset;
     }
   }

   &__contact {
     &:not(:last-of-type) {
       margin-bottom: 24px;
     }
   }

   &__contact-link {
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

   &__bottom {
     padding: 24px 0;
     border-top: 1px solid #233148;
   }
 }
</style>
