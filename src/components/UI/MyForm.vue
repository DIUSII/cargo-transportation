<template>
  <div class="fixed-container">
    <form class="form flex-center-between">
      <div>
        <span class="form__title">Быстрый заказ услуг</span>
        <span class="form__subtitle">Заполните, пожалуйста, форму </span>
      </div>
      <div>
        <my-input v-model="user.name" class="form__input" placeholder="Иван"/>
        <my-input v-model="user.phone" class="form__input" placeholder="+7 (_ _ _)  _ _ _  _ _  _ _" />
        <my-link>Перезвоните мне</my-link>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'my-form',
  data() {
    return {
      user: {
        name: '',
        phone: '',
      },
    };
  },
}
</script>

<style scoped>
 .form {
   background: #f2f2f2;
   border-radius: 5px;

   padding: 20px 80px;
 }

 .form__title {
   font-weight: 600;
   font-size: 19px;
   line-height: 23px;
   color: #353535;

   display: block;

   margin-bottom: 6px;
 }

 .form__subtitle {
   font-weight: 500;
   font-size: 15px;
   line-height: 18px;
   color: #818181;

   display: block;
 }

 .form__input {
   margin-right: 20px;
 }

 .form__input:last-child {
   margin-right: 40px;
 }
</style>