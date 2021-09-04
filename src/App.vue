<template>
  <div class="app">
    <header-main />
    <div class="app__container-relative">
      <all-type-transportation/>
      <my-form class="app__container-absolute"/>
    </div>
    <our-services />
    <our-car-park />
    <why-me></why-me>
  </div>
</template>

<script>
import HeaderMain from "@/components/HeaderMain";
import AllTypeTransportation from "@/components/AllTypeTransportation";
import OurServices from "@/components/OurServices";
import OurCarPark from "@/components/OurCarPark";
import WhyMe from "@/components/WhyMe";

export default {
  components: {
    HeaderMain,
    AllTypeTransportation,
    OurServices,
    OurCarPark,
    WhyMe,
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

.app__container-relative {
  position: relative;
}

.app__container-absolute {
  position: absolute;

  bottom: -33px;
  left: 0;
  right: 0;
}

.fixed-container {
  max-width: 1320px;
  width: 100%;

  padding: 0 20px;
  margin: 0 auto;
}

.align-center {
  display: flex;
  align-items: center;
}

.justify-center {
  display: flex;
  justify-content: center;
}
/* FIRST - ALIGN ITEMS, SECONDARY - JUSTIFY CONTENT*/
.flex-center-between {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.flex-start-between {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
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
