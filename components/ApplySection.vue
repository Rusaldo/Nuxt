<template>
  <div class="section apply">
    <div class="container">
      <ApplyForm class="apply__form" />
    </div>
  </div>
</template>

<script>
import ApplyForm from '~/components/form/ApplyForm.vue'

export default {
  components: {
    ApplyForm
  }
}
</script>

<style lang="scss" scoped>
  .apply {
    background: var(--primary-lightest-color);

    &__form {
      margin: 0 auto;
    }
  }
</style>
