<template>
  <div class="app">
    <TopBar class="app__top-bar" />
    <Header class="app__header" />

    <main class="app__main">
      <nuxt />
    </main>
    <Footer class="app__footer" />

    <ModalRoot />
  </div>
</template>

<script>
import TopBar from '~/components/layout/TopBar/TopBar.vue'
import Header from '~/components/layout/Header/Header.vue'
import Footer from '~/components/layout/Footer/Footer.vue'
import ModalRoot from '~/components/modal/ModalRoot.vue'

export default {
  components: {
    TopBar,
    Header,
    Footer,
    ModalRoot
  }
}
</script>

<style>

</style>
