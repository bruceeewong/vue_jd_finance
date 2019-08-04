<template>
  <section :class="[panelClass, cname]">
    <h4 v-if="title">-{{ title }}-</h4>
    <slot></slot>
  </section>
</template>

<script>
export default {
  name: 'v-panel',
  props: {
    cname: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
  },
  data () {
    return {
      panelClass: 'panel',
    };
  },
};
</script>

<style lang="scss">
@import "../../css/element.scss";

.panel {
  @include panel;
}
</style>
