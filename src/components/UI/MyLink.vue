<template>
  <a href="#" class="link"><slot></slot></a>
</template>

<script>
  export default {
    name: 'my-link',
  }
</script>

<style scoped>
  .link {
    font-weight: 600;
    font-size: 17px;
    line-height: 21px;
    color: #3284FF;

    text-decoration: none;
    border-bottom: 1px solid #3284ff;

    padding-bottom: 4px;
  }
</style>