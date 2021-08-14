<template>
  <div class="align-center all-type-transportation">
    <div class="all-type-transportation__container fixed-container">
      <h1 class="all-type-transportation__title">
        Все виды грузоперевозок
      </h1>
      <p class="all-type-transportation__subtitle">
        Мы бережно доставим любой груз от 1 тонны до 20 тонн в любую точку страны!
      </p>
      <ul class="all-type-transportation__list align-center">
        <li
          class="all-type-transportation__item text-500-gray"
          v-for="typeProduct in typesProduct"
          :key="typeProduct.id">
          {{ typeProduct.name }}
        </li>
      </ul>
      <my-button>Рассчитать стоимость</my-button>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        typesProduct: [
          {
            id: 0,
            name: 'скоропортящиеся',
          },
          {
            id: 1,
            name: 'крупногабаритные',
          },
          {
            id: 2,
            name: 'негабаритные грузы',
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .all-type-transportation {
    height: 670px;

    background-color: #040d21;
  }

  .all-type-transportation__title {
    font-weight: 800;
    font-size: 70px;
    line-height: 85px;
    color: #f3f3f3;

    max-width: 703px;

    margin-bottom: 41px;

  }

  .all-type-transportation__subtitle {
    font-size: 17px;
    line-height: 140%;
    color: #dbdbdb;

    max-width: 416px;

    margin-bottom: 20px;
  }

  .all-type-transportation__list {
    margin-left: 20px;
    margin-bottom: 40px;
  }

  .all-type-transportation__item {
    margin-right: 54px;
  }
</style>