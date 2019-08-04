<template>
  <v-panel :class="$style.panel">
    <ul :class="$style.content">
      <li>
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252" alt="">
      </li>
      <li>
        <div>
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t2971/333/1297567079/898/f2d2e00d/577dc28dNe5138337.png?width=108&height=108" alt="">
          <p>客户端</p>
        </div>
        <div>
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t2824/256/2966087355/831/188bfa25/577cf3dcN18aadbf2.png?width=108&height=108" alt="">
          <p>触屏版</p>
        </div>
        <div>
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t2920/282/1283157010/1040/23f1430b/577cf3e5N53f740b8.png?width=108&height=108" alt="">
          <p>电脑版</p>
        </div>
      </li>
      <li>
        <p>Copyright © 2004-2018 京东JD.com 版权所有</p>
      </li>
      <li>
        <p>投资有风险，购买需谨慎</p>
      </li>
      <li>
        <p>京东金融平台服务协议</p>
      </li>
      <li>
        <p>京东金融隐私政策</p>
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
  margin-bottom: 100px;

  .content {
    @include flex;
    background-color: #f5f5f5; 

    li {
      width: 100%;
      font-size: 24px;
      text-align: center;
      color: #999;

      > img {
        width: 100%;
        height: 143px;
      }

      > p {
        padding: 24px 0;
        border-top: 1px solid #ddd;
        line-height: 38px;
      }


      &:nth-child(2) {
        @include flex(row);
        box-sizing: border-box;
        height: 186px;

        > div {
          box-sizing: border-box;
          width: 33.33%;
          padding-top: 20px;
          text-align: center;

          > img {
            width: 90px;
            height: 90px;
          }

          > p {
            @include ellipsis;
            display: block;
            margin-top: 12px;
            font-size: 26px;
            text-align: center;
            color: #999;
          }
        }
      }
    }
  }
}
</style>