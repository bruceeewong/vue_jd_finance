<template>
  <v-panel title="新品推荐" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.arrow">更多尖货&gt;</div>
      <v-slider 
        :options="options"
        :slide-items="slideItems"
        cname="product-slider"
      ></v-slider>
    </section>
  </v-panel>
</template>

<script>
import VPanel from '../../../js/core/VPanel.vue';
import VSlider from '../../../js/core/VSlider.vue';

export default {
  name: 'product',
  components: {
    VPanel,
    VSlider,
  },
  data () {
    return {
      slideItems: [
        {
          href: 'home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t19063/263/1067257870/16513/d7360e92/5ab85da9N8af17d57.jpg?width=335&height=421'
        },
        {
          href: 'home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t12637/325/2370404484/14164/523e69a7/5ab85dd5Ndaf12da2.jpg?width=335&height=421'
        },
        {
          href: 'home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t17317/55/1066024964/35575/444c5252/5ab85ddeNaa593024.jpg?width=335&height=421'
        },
        {
          href: 'home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t16600/39/1049384083/42815/1727a973/5ab85debN56037cfc.jpg?width=335&height=421'
        },
      ],
      options: {
        slidesPerView: 2.3,
        spaceBetween: 30,
        freeMode: true,
      }
    };
  },
};
</script>

<style lang="scss">
.product-slider {
  .swiper-container {
    box-sizing: border-box;
    padding: 0 24px;
    
    .swiper-slide {
      a {
        display: inline-block;
        width: 100%;

        img {
          display: block;
          width: 100%; 
          height: 284px;
          border: 1px solid #fafafa;
        }
      }
    }
  }
}
</style>

<style lang="scss" module>
@import "../../../css/element.scss";

.panel {
  @include panel;

  .content {
    position: relative;
    padding-bottom: 40px;

    > .arrow {
      position: absolute;
      top: -70px;
      right: 30px;
      font-size: 28px;
      color: #999;
    }
  }
}
</style>

