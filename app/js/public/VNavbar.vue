<template>
  <v-panel :class="$style.panel">
    <ul :class="$style.content">
      <li>
        <router-link :to="{ name: 'home' }">
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t3451/188/644771475/2428/800d7cb7/580f2435Nbfaa8055.png?width=66&height=66" alt="">
          <p>首页</p>
        </router-link>
      </li>
      <li>
        <router-link :to="{ name: 'home' }">
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t3811/55/345433999/2930/116d3dd1/580f1e25N028a1f2c.png?width=66&height=66" alt="">
          <p>理财</p>
        </router-link>
      </li>
      <li>
        <router-link :to="{ name: 'home' }">
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t3343/179/621044750/1484/5af6b11a/580f50e4N005181d0.png?width=66&height=66" alt="">
          <p>白条</p>
        </router-link>
      </li>
      <li>
        <router-link :to="{ name: 'home' }">
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t3340/68/639059082/2591/800e2d6b/580f51cdN4caf20b2.png?width=66&height=66" alt="">
          <p>众筹</p>
        </router-link>
      </li>
      <li>
        <router-link :to="{ name: 'home' }">
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t3340/68/639059082/2591/800e2d6b/580f51cdN4caf20b2.png?width=66&height=66" alt="">
          <p>我的</p>
        </router-link>
      </li>
    </ul>
  </v-panel>
</template>

<script>
import VPanel from '../core/VPanel.vue';

export default {
  name: 'v-footer',
  components: {
    VPanel,
  },
};
</script>

<style lang="scss" module>
@import "../../css/element.scss";
@import "../../css/text.scss";

.panel {
  @include panel;
  position: fixed;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;
  height: 100px;
  margin: 0;

  .content {
    @include flex(row);
    justify-content: space-around;
    height: 100%;

    > li {
      text-align: center;

      a {
        text-decoration: none;
      }

      img {
        display: inline-block;
        width: 44px;
        height: 44px;
        margin: 12px auto 0;
      }

      p {
        font-size: 22px;
        color: #656565;
      }
    }

  }
}
</style>