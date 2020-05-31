<template>
  <form class="apply-form" @submit.prevent="handleSubmit">
    <h2 class="apply-form__title">Оставьте заявку</h2>
    <p class="apply-form__text">Наш менеджер поможет ответить на все интересующие вопросы, а также подобрать оптимальный способ получения кредита именно в вашем случае</p>
    <div class="apply-form__form-wrapper">
      <div class="apply-form__field">
        <BaseInput v-model="name"
                   type="text"
                   placeholder="Имя" />
      </div>
      <div class="apply-form__field">
        <BaseInput v-model="phone"
                   type="tel"
                   placeholder="Номер телефона" />
      </div>
      <div class="apply-form__field">
        <BaseButton type="primary" native-type="submit">Отправить заявку</BaseButton>
      </div>
    </div>
    <p class="apply-form__assent">
      &#128221; Я даю согласие ООО «Русалдо» на обработку моих <a class="link" href="#">персональных данных</a>
    </p>
  </form>
</template>

<script>
import BaseInput from '~/components/base/BaseInput.vue'
import BaseButton from '~/components/base/BaseButton.vue'

export default {
  name: 'ApplyForm',

  components: {
    BaseInput,
    BaseButton
  },

  data() {
    return {
      name: '',
      phone: ''
    }
  },

  methods: {
    handleSubmit() {
      this.clearForm()
      this.$emit('close')
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
    max-width: 500px;
    text-align: center;

    &__title {
      margin-bottom: 18px;
      font-size: 28px;
      color: var(--text-dark-color);
    }

    &__text {
      margin-bottom: 30px;
    }

    &__form-wrapper {
      margin-bottom: 18px;
    }

    &__field {
      &:not(:last-of-type) {
        margin-bottom: 24px;
      }
    }
  }

  .apply-form--modal {
    padding: 40px;
  }
</style>
