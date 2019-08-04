<template>
  <header :class="$style.header">
    <span :class="$style.left">
      <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
    </span>
    <v-btn :class="$style.btnDownload">APP下载</v-btn>
  </header>
</template>

<script>
import VBtn from '../core/VBtn.vue';

export default {
  name: 'v-header',
  components: {
    VBtn,
  },
};
</script>

<style lang="scss" module>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  height: 100px;
  background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
  background-size: auto 50%;
  font-size: 32px;
  line-height: 100px;
  color: #666;

  > .left {
    height: 30px;
    margin: 17px 0 0 18px;
    font-size: 28px;
    line-height: 30px;
  }

  > .btnDownload {
    float: right;
    min-width: 120px;
    height: 56px;
    padding: 0;
    margin: 28px 24px 0 0;
    border-radius: 4px;
    border-width: 0;
    font-size: 24px;
    line-height: 56px;
  }
}
</style>
