<template>
  <div class="our-services">
    <div class="fixed-container">
      <div class="our-services__container">
        <p class="our-services__about-company">
          Мы — <span class="our-services__about-company_weight_500">
          межрегиональная транспортная компания MTK-logistics</span>
          . Предоставляем услуги по перевозке всех видов
          грузов по Воронежу и России. Основной принцип нашей работы — надёжность и точность.
          Предлагаем сотрудничество в сфере грузоперевозок по выгодным условиям.
          Мы бережно доставим любой груз от 1 тонны до 20 тонн в любую точку страны!
          С нами, можно спать спокойно и не переживать за сохранность груза, потому что мы несем
          полную материальную ответственность.
        </p>
        <my-title :marginBottom="90">Всегда к вашим услугам собственный и наёмный транспорт</my-title>
        <ul class="our-services__list">
          <our-services-item
            v-for="servicesItem in servicesList"
            :key="servicesItem.id"
            :servicesItem="servicesItem"
          />
        </ul>
        <p class="our-services__about-company our-services__about-company_width_847">
          Мы бережно доставим любой груз от <span class="our-services__about-company_weight_500">
          1 тонны до 20 тонн</span> в любую точку страны!
          С нами, можно спать спокойно и не переживать за сохранность груза,
          потому что мы несем полную материальную ответственность.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
  import OurServicesItem from "@/components/OurServicesItem";

  export default {
    name: "OurServices",
    data() {
      return {
        servicesList: [
          {
            id: 0,
            title: 'Грузоперевозки  по Воронежу и области',
            moreDetails: true,
            img: 'car',
          },
          {
            id: 1,
            title: 'Междугородние перевозки от 1 до 20 тонн',
            moreDetails: true,
            img: 'map',
          },
          {
            id: 2,
            title: 'Доставка сборных грузов / догрузом / попутным грузом',
            moreDetails: true,
            img: 'orders',
          },
          {
            id: 3,
            title: 'Рефрежираторные, температурные перевозки',
            moreDetails: true,
            img: 'thermometer',
          },
          {
            id: 4,
            title: 'Перевозка опасных грузов',
            moreDetails: true,
            img: 'house',
          },
          {
            id: 5,
            title: 'Не знаете какой тип перевозок подойдёт именно Вам?',
            moreDetails: false,
            description: 'Заполните форму и лучшие менеджеры ответят на все Ваши вопросы',
            style: {
              background: '#fff',
              border: '2px solid #f2f2f2',
            },
          },
        ],
      }
    },
    components: {
      OurServicesItem,
    }
  }
</script>

<style scoped>
  .our-services {
    background-color: #fff;
  }

  .our-services__container {
    margin: 148px 0 170px;
  }

  .our-services__about-company {
    font-size: 20px;
    line-height: 140%;
    text-align: center;
    color: #353535;

    max-width: 1120px;

    margin: 0 auto 115px;

  }

  .our-services__about-company_weight_500 {
    font-weight: 500;
  }

  .our-services__about-company_width_847 {
    max-width: 847px;
  }

  .our-services__list {
    list-style: none;

    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    margin-bottom: 60px;
  }
</style>