<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__top-container">
        <div class="footer__about">
          <Logo class="footer__logo" light />
        </div>
<!--        <FooterNav />-->
        <div class="footer__contacts">
          <address class="footer__contact">
            <a class="footer__contact-link footer__contact-link--phone" href="tel:+74951350666">+7 (495) 135 0666</a>
            <br>
            <a class="footer__contact-link" href="mailto:contact@basiscredit.info">contact@basiscredit.info</a>
          </address>
          <address class="footer__contact">
            г. Москва, ул. Большая Грузинская, д. 20, пом. 5, офис 4
          </address>
        </div>
      </div>
      <div class="footer__bottom">
        <p>
          © ООО «Базис Кредит» 2020-{{ new Date().getFullYear() }}. Помощь в получении кредита на любые цели
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
  import Logo from '~/components/Logo.vue'
  import FooterNav from '~/components/FooterNav.vue'

  export default {
    components: {
      Logo,
      FooterNav
    }
  }
</script>

<style lang="scss" scoped>
 .footer {
   background-color: rgba(17, 20, 27, 0.95);
  // background-color: #323439;
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
       padding-top: 60px;
       padding-bottom: 60px;
     }

     @include laptop {
       padding-top: 100px;
       padding-bottom: 100px;
     }

     @include desktop {
       padding-top: 120px;
       gap: 60px;
     }
   }

   &__contacts {
     @include desktop {
       margin-left: auto;
       text-align: right;
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
