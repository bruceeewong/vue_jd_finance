<template>
  <div :class="$style.header">
    <span :class="$style.left">
      <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
    </span>
    <btn :class="$style.btnDownload">APP下载</btn>
  </div>
</template>

<script>
import btn from '../components/btn.vue';

export default {
  name: 'v-header',
  components: {
    btn
  }
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
  line-height: 100px;
  font-size: 32px;
  color: #666;
  background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
  background-size: auto 50%;

  > .left {
    height: 30px;
    line-height: 30px;
    font-size: 28px;
    margin: 17px 0 0 18px;
  }
  
  > .btnDownload {
    float: right;
    min-width: 120px;
    height: 56px;
    padding: 0;
    margin: 28px 24px 0 0;
    border-radius: 4px;
    border-width: 0;
    line-height: 56px;
    font-size: 24px;
  }
}
</style>
