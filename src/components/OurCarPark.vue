<template>
  <div class="our-car-park">
    <div class="fixed-container">
      <div class="our-car-park__container">
        <my-title :color="'#fff'" :marginBottom="9">Наш автопарк</my-title>
        <span class="our-car-park__subtitle">Собственный и наёмный транспорт: фуры и газели</span>
        <div class="our-car-park__group-list flex-start-between">
          <ul class="our-car-park__list">
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Полуприцеп</span>
            </li>
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Тентованные</span>
            </li>
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Тентовый транспорт</span>
            </li>
          </ul>
          <ul class="our-car-park__list">
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Открытые</span>
            </li>
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Бортовые</span>
            </li>
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Контейнеровозы</span>
            </li>
          </ul>
          <ul class="our-car-park__list">
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Изотермические</span>
            </li>
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Рефрижераторы</span>
            </li>
            <li class="our-car-park__item">
              <span class="our-car-park__item-text">Цельнометалические</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
  }
</script>

<style scoped>
  .our-car-park {
    background-color: #040d21;

    padding: 100px 0 144px;
  }

  .our-car-park__subtitle {
    font-weight: 500;
    font-size: 17px;
    line-height: 140%;
    color: #8193b2;

    display: block;

    text-align: center;

    margin-bottom: 81px;
  }

  .our-car-park__group-list {
    max-width: 800px;
    margin: 0 auto;
  }

  .our-car-park__item {
    font-weight: 500;
    font-size: 20px;
    line-height: 24px;
    color: #3284ff;

    margin-bottom: 17px;
  }

  .our-car-park__item:last-child {
    margin-bottom: 0;
  }

  .our-car-park__item-text {
    color: #fff;
  }
</style>