<template>
  <footer class="footer">
    <div class="footer__top">
      <div class="container footer__top-container">
        <FooterAbout />
        <FooterNav />
        <FooterContacts />
      </div>
    </div>
    <FooterBottom />
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
   background: var(--bg-gray-color);

   &__top {
    box-shadow: var(--footer-box-shadow);
   }

   &__top-container {
     padding-top: 60px;
     padding-bottom: 30px;
     display: grid;
     grid-template-columns: 250px 1fr auto;
     grid-auto-rows: auto;
     gap: 48px;

     @include tablet {
      grid-template-columns: 150px 1fr auto;
      gap: 24px;
     }

     @include tablet-small {
       grid-template-columns: 100%;
       padding-top: 30px;
     }
   }
 }
</style>
