<template>
  <div class="tab-switch">
    <div class="trans-zone" :style="styleObject">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'tab-switch',
  components: {},
  props: {
    index: {
      type: Number,
      default() {
        return 0;
      }
    }
  },
  data() {
    return {};
  },
  computed: {
    styleObject() {
      return {
        transform: `translateX(-${this.index * 25}%)`
      };
    }
  },
  watch: {},
  created() {},
  methods: {}
};
</script>

<style lang="scss">
.tab-switch {
  overflow: hidden;
  height: calc(100% - 50px);
  .trans-zone {
    height: 100%;
    width: 400%;
    display: flex;
    transition-duration: 0.3s;
  }
}
</style>
