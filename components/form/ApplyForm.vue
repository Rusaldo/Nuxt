<template>
  <form ref="form"
        class="apply-form"
        name="apply"
        data-netlify=true
        @submit.prevent="handleSubmit" >
<!--    <h2 class="apply-form__title">Оформить заявку на кредит</h2>-->
    <p class="apply-form__text">Наш менеджер поможет ответить на все интересующие вопросы</p>
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
        <BaseButton variant="accent" native-type="submit">Отправить заявку</BaseButton>
      </div>
    </div>
    <p class="apply-form__assent">
      &#128221; Я даю согласие ООО «Русалдо» на обработку моих <br> <a class="apply-form__link" href="#">персональных данных</a>
    </p>
  </form>
</template>

<script>
import BaseInput from '~/components/base/BaseInput.vue'
import BaseButton from '~/components/base/BaseButton.vue'
import ApplySuccess from '~/components/ApplySuccess.vue'
import ModalBus from '~/plugins/modalBus'

export default {
  name: 'ApplyForm',

  components: {
    BaseInput,
    BaseButton,
    ApplySuccess
  },

  data() {
    return {
      name: '',
      phone: ''
    }
  },

  methods: {
    handleSubmit() {
      if (!this.validate()) return
      const form = this.$refs.form
      console.log(form)
      const formData = new FormData(form)
      console.log(formData)
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
    max-width: 460px;
    text-align: center;

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
  }

  .apply-form--modal {
    padding: 40px;
  }
</style>
