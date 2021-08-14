<template>
  <button class="btn text-600-white">
    <slot></slot>
  </button>
</template>

<script>
  export default {
    name: 'my-button',
  }
</script>

<style scoped>
  .btn {
    padding: 19px 34px;
    background-color: #3284ff;
    border-radius: 5px;

    border: none;
  }
</style>