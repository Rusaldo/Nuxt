<template>
  <header class="header">
    <div class="container header__container">
      <Logo class="header__logo" />
      <NavBar class="header__navbar" />
      <div class="header__right">
        <BaseButton class="header__apply-button"
                    type="primary"
                    outlined
                    @click="openApplyModal">
          Оставить заявку &#9997;
        </BaseButton>
      </div>
    </div>
  </header>
</template>

<script>
import Logo from '~/components/Logo.vue'
import NavBar from '~/components/NavBar.vue'
import ModalBus from '~/plugins/modalBus'
import ApplyForm from '~/components/form/ApplyForm.vue'
import BaseButton from '~/components/base/BaseButton.vue'

export default {
  components: {
    Logo,
    NavBar,
    BaseButton
  },

  methods: {
    openApplyModal() {
      ModalBus.$emit('open', {
        component: ApplyForm,
        title: ''
      })
    }
  }
}
</script>

<style lang="scss" scoped>
  .header {
    box-shadow: var(--header-box-shadow);
  }

  .header__container {
    display: grid;
    grid-template-columns: auto 1fr auto;
    grid-template-areas: "logo navbar right";
    align-items: center;
    gap: 60px;
    grid-auto-rows: auto;
    padding-top: 24px;
    padding-bottom: 24px;

    @include tablet {
      gap: 10px 30px;
      grid-template-columns: auto 1fr;
      justify-content: space-between;
      justify-items: end;
      grid-template-areas: "logo right" "navbar navbar";
    }

    @include tablet-small {

    }

    @include mobile {
      flex-direction: column;
    }
  }

  .header__logo {
    grid-area: logo;
  }

  .header__navbar {
    grid-area: navbar;

    @include tablet {
      justify-self: center
    }
  }

  .header__right {
    grid-area: right;
  }
</style>
