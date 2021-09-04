<template>
  <li
    class="my-card flex-center-between"
    :style="{
      backgroundColor: item.style && item.style.background,
      border: item.style && item.style.border,
    }">
    <div class="my-card__container">
      <h3 class="my-card__title">{{ item.title }}</h3>
      <div v-if="item.moreDetails" class="my-card__more-details align-center">
        <span class="my-card__more-details-text">Подробнее</span>
        <img src="@/assets/images/ourServices/downArrow.svg" alt="downArrow">
      </div>
      <div class="flex-center-between">
        <p class="my-card__description" v-if="item.description">
          {{ item.description }}
        </p>
        <my-link v-if="item.orderServices">Заказать услугу</my-link>
      </div>
    </div>
    <img
      v-if="item.img"
      :src="require(`@/assets/images/${item.img}.svg`)"
      :alt="item.img"
    >
  </li>
</template>

<script>
  export default {
    name: 'MyCard',
    props: {
      item: {
        id: Number,
        title: String,
        img: String,
        moreDetails: {
          type: Boolean,
          default: true,
        },
        description: {
          type: Boolean,
          default: true,
        },
        orderServices: {
          type: Boolean,
          default: true,
        },
        style: {
          background: {
            type: String,
            default: '#f2f2f2',
          },
          border: {
            type: String,
            default: 'none',
          },
        },
      },
    },
  }
</script>

<style scoped>
  .my-card {
    background: #f2f2f2;
    border-radius: 17px;

    width: 100%;
    max-width: 630px;
    min-height: 257px;

    margin-bottom: 20px;
    padding: 54px 45px 54px 54px;
  }

  .my-card__container {
    width: 100%;
  }

  .my-card__title {
    font-weight: bold;
    font-size: 20px;
    line-height: 140%;
    color: #2e2e2e;

    max-width: 330px;

    margin-bottom: 25px;
  }

  .my-card__more-details {
    margin-bottom: 20px;
  }

  .my-card__more-details-text {
    font-size: 17px;
    line-height: 21px;
    color: #2e2e2e;

    margin-right: 10px;
  }

  .my-card__description {
    font-weight: 500;
    font-size: 17px;
    line-height: 140%;
    color: #353535;

    max-width: 275px;
  }
</style>