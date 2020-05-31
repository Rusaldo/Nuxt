<template>
  <div class="app">
    <Header class="app__header" />

    <main class="app__main">
      <nuxt />
    </main>
    <Footer class="app__footer" />

    <ModalRoot />
  </div>
</template>

<script>
  import Header from '~/components/Header.vue'
  import Footer from '~/components/Footer.vue'
  import ModalRoot from '~/components/modal/ModalRoot.vue'

  export default {
    components: {
      Header,
      Footer,
      ModalRoot
    }
  }
</script>

<style>

</style>
