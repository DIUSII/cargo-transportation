<template>
  <header class="header">
    <div class="header__container fixed-container">
      <img src="@/assets/images/headerMain/logo.svg" alt="logo" class="header__logo">
      <div class="header__container">
        <nav class="header__nav">
          <ul class="header__list">
            <li class="header__item text-500-gray" v-for="menu in menus" :key="menu.id">
              {{ menu.name }}
            </li>
          </ul>
        </nav>
        <div class="header__contact-container">
          <div class="header__phone-container align-center">
            <img src="@/assets/images/headerMain/phone.svg" alt="phone" class="header__contact-img">
            <a href="tel:+79036526722" class="header__contact-info header__contact-phone text-600-white">
              +7 (903) 652 67 22
            </a>
            <img src="@/assets/images/headerMain/downArrow.svg" alt="downArrow">
          </div>
          <div class="header__email-container align-center">
            <img src="@/assets/images/headerMain/mail.svg" alt="mail" class="header__contact-img">
            <a href="mailto:manager@mtk-logistics.ru" class="header__contact-info text-600-white">
              manager@mtk-logistics.ru
            </a>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
  export default {
    data() {
      return {
        menus: [
          {
            id: 0,
            name: 'Услуги',
          },
          {
            id: 1,
            name: 'Калькулятор',
          },
          {
            id: 2,
            name: 'Как мы работаем',
          },{
            id: 3,
            name: 'Отзывы',
          },
          {
            id: 4,
            name: 'Контакты',
          },
        ],
      }
    }
  }
</script>

<style scoped>
  .header {
    background-color: #040d21;

    padding-top: 45px;
  }

  .header__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .header__container {
    display: flex;
    align-items: center;
  }

  .header__logo {

  }

  .header__list {
    list-style: none;
    display: flex;
    align-items: center;
  }

  .header__item {
    text-decoration: none;
    margin-right: 49px;
  }

  .header__phone-container {
    margin-bottom: 11px;
  }

  .header__contact-info {
    font-size: 17px;
    font-weight: 600;
    line-height: 21px;
    text-decoration: none;

    color: #fff;
  }

  .header__contact-phone {
    margin-right: 9px;
  }

  .header__contact-img {
    margin-right: 18px;
  }

</style>