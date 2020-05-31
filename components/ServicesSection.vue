<template>
  <section class="section services">
    <div class="container">
      <ul class="services__list">
        <ServiceCard v-for="service in services"
                     :key="service.id"
                     :service="service" />
      </ul>
    </div>
  </section>
</template>

<script>
import ServiceCard from '~/components/ServiceCard.vue'

export default {
  components: {
    ServiceCard
  },

  data() {
    return {
      services: [
        {
          id: '1',
          title: 'Потребительский кредит (кредит наличными)',
          url: '#'
        },
        {
          id: '2',
          title: 'Ипотечное кредитование',
          url: '#'
        },
        {
          id: '3',
          title: 'Кредит под залог автомобиля',
          url: '#'
        },
        {
          id: '4',
          title: 'Кредит под залог недвижимости',
          url: '#'
        },
        {
          id: '5',
          title: 'Кредит для бизнеса',
          url: '#'
        },
        {
          id: '6',
          title: 'Рефинансирование кредита',
          url: '#'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .services {

    &__list {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-auto-rows: auto;
      gap: 30px;
      justify-content: center;

      @include tablet {
        grid-template-columns: repeat(2, 1fr);
      }

      @include tablet-small {
        grid-template-columns: auto;
        gap: 18px;
      }
    }
  }
</style>
