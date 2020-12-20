<template>
  <section class="section hero">
    <div class="container hero__container">
      <div class="hero__sub-heading">
        Кредитный брокер
      </div>
      <div class="hero__heading">
        Помогаем получать <br>
        кредиты в банках
      </div>
      <div class="hero__description">
        Одобрим кредит на любые цели за 1 день
      </div>
      <BaseButton class="hero__btn"
                  variant="accent"
                  tag="a"
                  href="#apply">
        Оставить заявку
      </BaseButton>
    </div>
  </section>
</template>

<script>
import BaseButton from '~/components/base/BaseButton.vue'
import ApplyForm from '~/components/form/ApplyForm.vue'
import ModalBus from '~/plugins/modalBus'

export default {
  components: {
    BaseButton,
    ApplyForm
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
  .hero {
    min-height: calc(100vh - 61px);
    background-image: url('/hero.jpg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
    display: flex;
    align-items: center;
    text-align: center;

    @include tablet {
      text-align: left;
    }

    @include laptop {
      height: 900px;
    }

    &__container {
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      align-items: center;

      @include tablet {
        align-items: flex-start;
      }
    }

    &__sub-heading {
      font-size: 15px;
      position: relative;
      color: var(--accent-color);
      text-transform: uppercase;
      margin-bottom: 24px;
      font-weight: 500;
      padding-bottom: 24px;

      &::before {
        content: '';
        position: absolute;
        width: 54px;
        height: 2px;
        background: var(--accent-color);
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);

        @include tablet {
          left: 0;
          top: 50%;
          transform: translateY(-50%);
        }
      }

      @include tablet {
        padding-left: 68px;
        padding-bottom: 0;
        font-size: 18px;
      }
    }

    &__heading {
      font-size: 29px;
      margin-bottom: 30px;
      font-weight: 800;
      color: #000;
      line-height: 1.2;

      @include tablet {
        font-size: 50px;
      }

      @include desktop {
        font-size: 65px;
      }
    }

    &__description {
      color: #000;
      max-width: 500px;
      font-size: 18px;
      margin-bottom: 30px;
      line-height: 30px;

      @include tablet {
        margin-bottom: 50px;
      }
    }
  }
</style>
