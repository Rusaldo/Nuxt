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
              <li>На любые цели</li>
              <li>Ставки от 6%</li>
              <li>Сумма до 10 млн руб</li>
            </ul>
          </div>
        </li>


        <li class="services__card">
          <IconExchange class="services__icon" />
          <h3 class="services__heading">
            Рефинансирование
          </h3>
          <div class="services__description">
            <p>Объединим несколько кредитов в один</p>
            <p>Уменьшим ставку по действующему кредиту с возможностью получения дополнительной суммы</p>
            <p>Самые выгодные условия на рынке</p>
            <p>Быстрое рассмотрение заявки</p>
            <p>Минимальный пакет документов</p>
          </div>
        </li>


        <li class="services__card">
          <IconBuildings class="services__icon" />
          <h3 class="services__heading">
            Ипотечный кредит
          </h3>
          <div class="services__description">
            <ul>
              <li>Льготные программы ипотечного кредитования</li>
              <li>Выгодные ставки от 5%</li>
              <li>До 30 млн руб.</li>
              <li>Возможность получения ипотеки без первоначального взноса</li>
            </ul>
          </div>
        </li>


        <li class="services__card">
          <div class="services__icon">
            Icon
          </div>
          <h3 class="services__heading">
            Залоговое финансирование
          </h3>
          <div class="services__description">
            <ul>
              <li>Без подтверждения цели кредита</li>
              <li>Под залог недвижимости или транспортного средства</li>
              <li>Гибкие условия кредитования</li>
              <li>Сумма до 15 млн руб.</li>
              <li>Комфортный срок от 1 года до 20 лет</li>
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

      @include tablet {
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
  }
</style>
