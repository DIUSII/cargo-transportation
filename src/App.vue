<template>
  <header-main />
  <all-type-transportation />
</template>

<script>
import HeaderMain from "@/components/HeaderMain";
import AllTypeTransportation from "@/components/AllTypeTransportation";

export default {
  components: {
    HeaderMain,
    AllTypeTransportation,
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Montserrat', sans-serif;
}

.fixed-container {
  max-width: 1240px;
  width: 100%;

  padding: 0 20px;
  margin: 0 auto;
}

.align-center {
  display: flex;
  align-items: center;
}

.text-500-gray {
  font-weight: 500;
  font-size: 17px;
  line-height: 21px;
  color: #e3e3e3;
}

.text-600-white {
  font-weight: 600;
  font-size: 17px;
  line-height: 21px;
  color: #fff;
}

</style>
