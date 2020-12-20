<template>
  <div class="section apply">
    <div class="container">
      <SectionTitle center>Оформить заявку на кредит</SectionTitle>
      <ApplyForm class="apply__form" />
    </div>
  </div>
</template>

<script>
import ApplyForm from '~/components/form/ApplyForm.vue'
import SectionTitle from '~/components/SectionTitle.vue'

export default {
  components: {
    SectionTitle,
    ApplyForm
  }
}
</script>

<style lang="scss" scoped>
  .apply {
    &__form {
      margin: 0 auto;
    }
  }
</style>
