<template>
  <v-panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <dl 
        v-for="item in items"
        :key="item.title"
        :class="$style.item"
      >
        <dt>{{ item.title }}<span>{{ item.sub }}</span></dt>
        <dd>{{ item.rate }}</dd>
        <dd>{{ item.text }}</dd>
      </dl> 
    </section>
  </v-panel>
</template>

<script>
import VPanel from '../../../js/core/VPanel.vue';

export default {
  name: 'money',
  components: {
    VPanel,
  },
  data () {
    return {
      items: [
        {
          title: '定期理财',
          sub: '理财首选',
          rate: '5.60%',
          text: '历史年化回报率',
        },
        {
          title: '小白理财',
          sub: '理财首选',
          rate: '4.22%',
          text: '7日年化收益率',
        },
        {
          title: '月月盈',
          sub: '养老保障',
          rate: '5%',
          text: '七日年化收益率',
        },
        {
          title: '小白基金',
          sub: '天天赚钱',
          rate: '4.27%',
          text: '7日年化收益率',
        },
      ],
    };
  }
};
</script>

<style lang="scss" module>
@import "../../../css/element.scss";
@import "../../../css/text.scss";

.panel {
  @include panel;

  .content {
    @include list(row);
    justify-content: space-around;
    box-sizing: border-box;

    &:after {
      content: " ";
      display: block;
      position: relative;
      top: -208px;
      width: 100%;
      height: 1px;
      border-bottom: 1px solid #eee;
    }

    .item {
      box-sizing: border-box;
      position: relative;
      width: 50%;
      padding: 34px 16px;

      &:after {
        content: " ";
        display: block;
        position: absolute;
        top: 50%;
        right: 0;
        width: 1px;
        height: 136px;
        margin-top: -68px;
        border-right: 1px solid #eee;

      }

      &:nth-child(2n) {
        &:after {
          display: none;
        }
      }

      dt {
        font-size: 30px;
        line-height: 42px;
        color: #333;

        span {
          padding: 0 8px;
          border: 1px solid #ff5155;
          font-size: 22px;
          vertical-align: 1px;
          color: #ff5155;
        }
      }

      dd {
        &:nth-child(2) {
          @include ellipsis;
          height: 58px;
          line-height: 58px;
          font-size: 44px;
          font-weight: 700;
          color: #ff5155;
        }

        &:nth-child(3) {
          @include ellipsis;
          height: 34px;
          line-height: 34px;
          font-size: 24px;
          font-weight: 700;
          color: #999;
        }
      }
      
    }

    
  }
}
</style>