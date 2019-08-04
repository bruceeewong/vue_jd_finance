<template>
  <div>
    <v-header></v-header>
    <h-slider></h-slider>
  </div>
</template>

<script>
import VHeader from "../../layout/VHeader.vue";
import HSlider from "./hslider.vue";

export default {
  name: 'home',
  components: {
    VHeader,
    HSlider
  }
};
</script>

<style lang="scss" scoped>

</style>