<template>
  <div class="why-me">
    <div class="fixed-container">
      <my-title :marginBottom="90">Почему выбирают нас</my-title>
      <ul class="why-me__list">
        <my-card v-for="cause in causesWhyWe" :item="cause" :key="cause.id"/>
      </ul>
      <p class="why-me__description">
        Мы — <span class="why-me__description_weight_500">межрегиональная транспортная компания MTK-logistics.</span>
        Предоставляем услуги по перевозке всех видов грузов по Воронежу и России.
        Основной принцип нашей работы — надёжность и точность. Предлагаем
        сотрудничество в сфере грузоперевозок по выгодным условиям.
      </p>
      <div class="about-us why-me__about-us  flex-center-between">
        <div class="about-us__item justify-center">
          <h3 class="about-us__title">197</h3>
          <span class="about-us__description">тонн груза ежедневно</span>
        </div>
        <div class="about-us__item justify-center">
          <h3 class="about-us__title">93</h3>
          <span class="about-us__description">единиц транспорта в пути</span>
        </div>
        <div class="about-us__item justify-center">
          <h3 class="about-us__title">9352</h3>
          <span class="about-us__description">городов доставки</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        orderServices: false,
      };
    },
    computed: {
      causesWhyWe() {
        return ([
          {
            id: 0,
            title: 'Предложим оптимальную стоимость перевозки',
            img: 'whyMe/axe',
            orderServices: this.orderServices,
          },
          {
            id: 1,
            title: 'Подберём транспорт под вашу задачу',
            img: 'whyMe/car',
            orderServices: this.orderServices,
          },
          {
            id: 2,
            title: 'Предоставим услуги страхования груза',
            img: 'whyMe/case',
            orderServices: this.orderServices,
          },
          {
            id: 3,
            title: 'Быстро оформим все документы. Работаем с НДС',
            img: 'whyMe/documents',
            orderServices: this.orderServices,
          },
        ]);
      }
    }
  }
</script>

<style scoped>
  .why-me {
    padding: 170px 0 115px;
  }

  .why-me__list {
    list-style: none;

    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    margin-bottom: 60px;
  }

  .why-me__description {
    font-size: 20px;

    text-align: center;
    color: #353535;

    max-width: 850px;
    margin: 0 auto 115px;

  }

  .why-me__description_weight_500 {
    font-weight: 500;
  }

  .about-us {
    background: #f2f2f2;
    border-radius: 5px;
    padding: 25px 0;

    height: 200px;
  }

  .about-us__item {
    padding: 0 132px;
    height: 100%;

    flex-direction: column;

    text-align: center;

    border-left: 2px solid #dcdcdc;
  }

  .about-us__item:first-child {
    border-left: none;
  }

  .about-us__title {
    font-size: 30px;
    font-weight: 600;

    color: #2e2e2e;

    margin-bottom: 10px;
  }

  .about-us__description {
    font-weight: 500;
    font-size: 17px;

    color: #353535;
  }
</style>