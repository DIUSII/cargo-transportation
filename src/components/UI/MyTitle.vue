<template>
  <h2 class="title" :style="{marginBottom: marginBottom + 'px', color: color}"><slot></slot></h2>
</template>

<script>
  export default {
    name: 'my-title',
    props: {
      marginBottom: Number,
      color: {
        type: String,
        default: '#2e2e2e',
      }
    }
  }
</script>

<style scoped>
  .title {
    font-weight: bold;
    font-size: 30px;
    line-height: 37px;

    text-align: center;
  }
</style>