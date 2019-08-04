<template>
  <div id="home">
    <v-header></v-header>
    <home-slider></home-slider>
  </div>
</template>

<script>
import VHeader from '../../js/public/VHeader.vue';
import HomeSlider from './components/HomeSlider.vue';

export default {
  name: 'home',
  components: {
    VHeader,
    HomeSlider,
  },
};
</script>

<style lang="scss" scoped>

</style>
