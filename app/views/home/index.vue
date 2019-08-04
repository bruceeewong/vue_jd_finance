<template>
  <div id="home">
    <v-header></v-header>
    <home-slider></home-slider>
    <novice></novice>
    <borrow></borrow>
    <money></money>
    <product></product>
    <life></life>
    <v-footer></v-footer>
    <v-navbar></v-navbar>
  </div>
</template>

<script>
import VHeader from '../../js/public/VHeader.vue';
import VFooter from '../../js/public/VFooter.vue';
import VNavbar from '../../js/public/VNavbar.vue';
import HomeSlider from './components/HomeSlider.vue';
import Novice from './components/Novice.vue';
import Borrow from './components/Borrow.vue';
import Money from './components/Money.vue';
import Money from './components/Money.vue';
import Product from './components/Product.vue';
import Life from './components/Life.vue';

export default {
  name: 'home',
  components: {
    VHeader,
    VFooter,
    VNavbar,
    HomeSlider,
    Novice,
    Borrow,
    Money,
    Product,
    Life,
  },
};
</script>

<style lang="scss" scoped>

</style>
