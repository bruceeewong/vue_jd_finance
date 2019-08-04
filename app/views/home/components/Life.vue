<template>
  <v-panel title="生活服务" :class="$style.panel">
    <ul :class="$style.content">
      <li :class="$style.item"
        v-for="item in items"
        :key="item.desc"
      >
        <img :src="item.src" :alt="item.desc">
        <p>{{ item.desc }}</p>
        <p
          v-if="item.isNew"
          :class="$style.new"
        >全新升级</p>
      </li>
    </ul>
  </v-panel>
</template>

<script>
import VPanel from '../../../js/core/VPanel.vue';

export default {
  name: 'life',
  components: {
    VPanel,
  },
  data () {
    return {
      items: [
        {
          desc: '旅游',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90'
        },
        {
          desc: '医美',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90',
          isNew: true
        },
        {
          desc: '房抵贷',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88'
        },
        {
          desc: '驾校',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90'
        },
        {
          desc: '分期用',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t14896/125/1435676873/3668/a8b392f7/5a4f26edN6cdfda66.png?width=88&height=88'
        }
      ]
    }
  }
};
</script>

<style lang="scss" module>
@import "../../../css/element.scss";
@import "../../../css/text.scss";

.panel {
  @include panel;

  .content {
    @include flex(row);
    box-sizing: border-box;
    padding-bottom: 40px;

    .item {
      width: 20%;
      text-align: center;

      img {
        width: 90px;
        height: 90px;
      }

      p {
        @include ellipsis;

        margin-top: 12px;
        font-size: 26px;
        color: #666;
      }

      .new {
        color: #ff801a;
      }
    }
  }
}
</style>