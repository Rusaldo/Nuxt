<template>
  <form ref="form"
        class="apply-form"
        data-netlify="true"
        name="apply"
        @submit.prevent="handleSubmit" >
    <p class="apply-form__text">Наш специалист свяжется с вами в ближайшее время</p>
    <div class="apply-form__form-wrapper">
      <div class="apply-form__field">
        <BaseInput v-model="name"
                   type="text"
                   name="name"
                   placeholder="Имя" />
      </div>
      <div class="apply-form__field">
        <BaseInput v-model="phone"
                   type="tel"
                   name="phone"
                   placeholder="Номер телефона" />
      </div>
      <div class="apply-form__field">
        <BaseInput v-model="email"
                   type="email"
                   name="email"
                   placeholder="Email" />
      </div>
      <div class="apply-form__field">
        <BaseInput v-model="sum"
                   type="number"
                   name="sum"
                   placeholder="Cумма кредита (руб.)" />
      </div>
      <div class="apply-form__field">
        <BaseButton variant="accent" native-type="submit" block>Отправить заявку</BaseButton>
      </div>
    </div>
    <p class="apply-form__assent">
      Нажимая кнопку «Отправить заявку» вы принимаете <br>
      <nuxt-link class="apply-form__policy" to="/policy/">условия передачи персональных данных</nuxt-link>.
    </p>
  </form>
</template>

<script>
import BaseInput from '~/components/base/BaseInput.vue'
import BaseButton from '~/components/base/BaseButton.vue'
import ApplySuccess from '~/components/ApplySuccess.vue'
import IconContract from '~/components/icons/IconContract'
import ModalBus from '~/plugins/modalBus'

export default {
  name: 'ApplyForm',

  components: {
    BaseInput,
    BaseButton,
    ApplySuccess,
    IconContract
  },

  data() {
    return {
      name: '',
      phone: '',
      email: '',
      sum: ''
    }
  },

  methods: {
    handleSubmit(e) {
      e.preventDefault()
      if (!this.validate()) return
      console.log('Validaton passed')
      const form = this.$refs.form
      const formData = new FormData(form)
      fetch('/', {
        method: 'POST',
        headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
        body: new URLSearchParams(formData).toString()
      })
        .then(() => {
          console.log('Form successfully submitted')
          this.clearForm()
          this.$emit('close')
          this.onSuccess()
        })
        .catch(error => {
          console.error(error)
        })
    },
    validate() {
      return this.name.length && this.phone.length
    },
    onSuccess() {
      ModalBus.$emit('open', {
        component: ApplySuccess,
        title: 'Ваша заявка принята'
      })
    },
    clearForm() {
      this.name = ''
      this.phone = ''
    }
  }
}
</script>

<style lang="scss" scoped>
  .apply-form {
    max-width: 450px;
    text-align: center;
    margin: 0 auto;

    &__title {
      margin-bottom: 18px;
      font-size: 28px;
      color: var(--text-dark-color);
    }

    &__text {
      margin-bottom: 30px;
      font-size: 18px;
    }

    &__form-wrapper {
      margin-bottom: 18px;
    }

    &__field {
      &:not(:last-of-type) {
        margin-bottom: 24px;
      }
    }

    &__assent {
      font-size: 14px;
    }

    &__link {
      text-decoration: underline;
    }

    &__icon {
      width: 1.2em;
      height: 1.2em;
      vertical-align: middle;
      margin-right: 6px;
    }

    &__policy {
      text-decoration: underline;
    }
  }

  .apply-form--modal {
    padding: 40px;
  }
</style>
