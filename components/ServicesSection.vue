<template>
  <section class="section section--bg-gray services">
    <div class="container">
      <SectionTitle>Услуги</SectionTitle>
      <ul class="services__list">
        <ServiceCard v-for="service in services"
                     :key="service.id"
                     :service="service" />
      </ul>
    </div>
  </section>
</template>

<script>
import SectionTitle from '~/components/SectionTitle.vue'
import ServiceCard from '~/components/ServiceCard.vue'

export default {
  components: {
    SectionTitle,
    ServiceCard
  },

  data() {
    return {
      services: [
        {
          id: '1',
          title: 'Потребительский кредит',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae, vitae?',
          url: '#'
        },
        {
          id: '2',
          title: 'Ипотечное кредитование',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae, vitae?',
          url: '#'
        },
        {
          id: '3',
          title: 'Кредит под залог автомобиля',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae, vitae?',
          url: '#'
        },
        {
          id: '4',
          title: 'Кредит под залог недвижимости',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae, vitae?',
          url: '#'
        },
        {
          id: '5',
          title: 'Кредит для бизнеса',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae, vitae?',
          url: '#'
        },
        {
          id: '6',
          title: 'Рефинансирование кредита',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae, vitae?',
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
      grid-template-columns: 100%;
      gap: 50px;
      grid-auto-rows: auto;
      justify-content: center;

      @include tablet {
        grid-template-columns: repeat(2, 1fr);
      }

      @include desktop {
        grid-template-columns: repeat(3, 1fr);
        gap: 50px;
      }
    }
  }
</style>
