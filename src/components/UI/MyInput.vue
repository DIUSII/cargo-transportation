<template>
  <input type="text" class="input" :value="modelValue" @input="updateInput">
</template>

<script>
  export default {
    name: 'my-input',
    props: {
      modelValue: [String, Number]
    },
    methods: {
      updateInput(event) {
        this.$emit('update:modelValue', event.target.value)
      }
    }
  }
</script>

<style scoped>
 .input {
   border: 1px solid #bdbdbd;
   border-radius: 5px;

   min-width: 250px;

   padding: 20px 0 20px 30px;
 }
</style>