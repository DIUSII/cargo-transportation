<template>
  <li
    class="our-services-item flex-start-between"
    :style="{
      backgroundColor: servicesItem.style && servicesItem.style.background,
      border: servicesItem.style && servicesItem.style.border,
    }">
    <div class="our-services-item__container">
      <h3 class="our-services-item__title">{{ servicesItem.title }}</h3>
      <div v-if="servicesItem.moreDetails" class="our-services-item__more-details align-center">
        <span class="our-services-item__more-details-text">Подробнее</span>
        <img src="@/assets/images/ourServices/downArrow.svg" alt="downArrow">
      </div>
      <div class="flex-center-between">
        <p class="our-services-item__description" v-if="servicesItem.description">
          {{ servicesItem.description }}
        </p>
        <my-link>Заказать услугу</my-link>
      </div>
    </div>
    <img
      v-if="servicesItem.img"
      :src="require(`@/assets/images/ourServices/item/${servicesItem.img}.svg`)"
      :alt="servicesItem.img"
    >
  </li>
</template>

<script>
  export default {
    props: {
      servicesItem: {
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
  .our-services-item {
    background: #f2f2f2;
    border-radius: 17px;

    width: 100%;
    max-width: 630px;

    margin-bottom: 20px;
    padding: 54px 45px 54px 54px;
  }

  .our-services-item__container {
    width: 100%;
  }

  .our-services-item__title {
    font-weight: bold;
    font-size: 20px;
    line-height: 140%;
    color: #2e2e2e;

    max-width: 330px;

    margin-bottom: 25px;
  }

  .our-services-item__more-details {
    margin-bottom: 20px;
  }

  .our-services-item__more-details-text {
    font-size: 17px;
    line-height: 21px;
    color: #2e2e2e;

    margin-right: 10px;
  }

  .our-services-item__description {
    font-weight: 500;
    font-size: 17px;
    line-height: 140%;
    color: #353535;

    max-width: 275px;
  }
</style>