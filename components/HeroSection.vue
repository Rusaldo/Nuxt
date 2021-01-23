<template>
  <section class="section hero">
    <div class="container hero__container">
      <!-- <div class="hero__sub-heading">
        Кредитный брокер
      </div> -->
      <div class="hero__heading">
        Гарантированная помощь <br>
        в получении кредита
      </div>
      <div class="hero__description">
        <div class="hero__feature">Одобрим заявку в день обращения</div>
        <div class="hero__feature">Без поручителей и предоплат</div>
        <div class="hero__feature">Только паспорт и СНИЛС</div>
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

    @include tablet {
      text-align: left;
    }

    @include laptop {
      height: 700px;
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
      }

      @include tablet {
        padding-left: 68px;
        font-size: 18px;
      }
    }

    &__heading {
      font-size: 24px;
      margin-bottom: 30px;
      font-weight: 700;
      color: var(--primary-color);
      line-height: 1.2;
      position: relative;
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

        @include small-tablet {
          display: none;
        }
      }


      @include tablet {
        color: black;
        font-size: 40px;
      }

      @include desktop {
        font-size: 55px;
      }
    }

    &__description {
      color: #000;
      max-width: 500px;
      font-size: 18px;
      margin-bottom: 40px;
      line-height: 30px;

      @include tablet {
        margin-bottom: 50px;
        font-size: 22px;
      }
    }

    &__feature {
      position: relative;

      &:before {
        content: '';
        display: inline-block;
        width: 8px;
        height: 8px;
        background-color: var(--accent-color);
        border-radius: 30px;
        margin-bottom: 3px;
        margin-right: 12px;
      }
    }

    &__btn {
      width: 100%;

      @include small-tablet {
        width: auto;
      }
    }
  }
</style>
