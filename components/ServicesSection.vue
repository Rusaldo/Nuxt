<template>
  <section class="section section--bg-gray services">
    <div class="container">
      <SectionTitle>Услуги</SectionTitle>

      <ul class="services__list">
        <li class="services__card">
          <IconDollar class="services__icon" />
          <h3 class="services__heading">
            Потребительский кредит
          </h3>
          <div class="services__description">
            <ul>
              <li class="services__list-item">На любые цели</li>
              <li class="services__list-item">Ставки от 6%</li>
              <li class="services__list-item">Сумма до 10 млн руб</li>
            </ul>
          </div>
        </li>


        <li class="services__card">
          <IconExchange class="services__icon" />
          <h3 class="services__heading">
            Рефинансирование
          </h3>
          <div class="services__description">
            <ul>
              <li class="services__list-item">Объединим несколько кредитов в один</li>
              <li class="services__list-item">Уменьшим ставку по действующему кредиту с возможностью получения дополнительной суммы</li>
              <li class="services__list-item">Самые выгодные условия на рынке</li>
              <li class="services__list-item">Быстрое рассмотрение заявки</li>
              <li class="services__list-item">Минимальный пакет документов</li>
            </ul>
          </div>
        </li>


        <li class="services__card">
          <IconBuildings class="services__icon" />
          <h3 class="services__heading">
            Ипотечный кредит
          </h3>
          <div class="services__description">
            <ul>
              <li class="services__list-item">Льготные программы ипотечного кредитования</li>
              <li class="services__list-item">Выгодные ставки от 5%</li>
              <li class="services__list-item">До 30 млн руб.</li>
              <li class="services__list-item">Возможность получения ипотеки без первоначального взноса</li>
            </ul>
          </div>
        </li>


        <li class="services__card">
          <IconDollar class="services__icon" />
          <h3 class="services__heading">
            Залоговое финансирование
          </h3>
          <div class="services__description">
            <ul>
              <li class="services__list-item">Без подтверждения цели кредита</li>
              <li class="services__list-item">Под залог недвижимости или транспортного средства</li>
              <li class="services__list-item">Гибкие условия кредитования</li>
              <li class="services__list-item">Сумма до 15 млн руб.</li>
              <li class="services__list-item">Комфортный срок от 1 года до 20 лет</li>
            </ul>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import SectionTitle from '~/components/SectionTitle.vue'
import IconBuildings from '~/components/icons/IconBuildings'
import IconExchange from '~/components/icons/IconExchange'
import IconDollar from '~/components/icons/IconDollar'

export default {
  components: {
    SectionTitle,
    IconBuildings,
    IconExchange,
    IconDollar
  }
}
</script>

<style lang="scss" scoped>
  .services {

    &__list {
      display: grid;
      grid-template-columns: 100%;
      gap: 30px;
      grid-auto-rows: auto;
      justify-content: center;

      @include laptop {
        grid-template-columns: repeat(2, 1fr);
        gap: 60px;
      }
    }

    &__card {
      padding: 42px 18px;
      position: relative;
      background: #fff;
      text-align: center;

      @include tablet {
        padding: 42px 30px;
      }
    }

    &__icon {
      width: 68px;
      height: 68px;
      color: var(--accent-color);
      margin-bottom: 30px;
    }

    &__heading {
      color: var(--primary-color);
      font-size: 24px;
      font-weight: 500;
      margin-bottom: 18px;

      @include tablet {
        font-size: 29px;
        margin-bottom: 30px;
      }
    }

    &__description {
      color: #57667e;
      font-size: 16px;

      @include tablet {
        font-size: 18px;
      }
    }

    &__list-item {
      &::before {
        content: '—';
        margin-right: 6px;
        color: var(--primary-color);
      }

      &:not(:last-child) {
        margin-bottom: 6px;
      }
    }
  }
</style>
