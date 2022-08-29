<template>
  <div
    class="es-header-container"
    :style="{
      'background-color': bgcolor,
      color: color,
      'font-size': fontsize + 'px'
    }"
  >
    {{ title }}
  </div>
</template>

<script>
export default {
  name: 'EsHeader',
  props: {
    title: {
      default: 'es-header',
      type: String
    },
    bgcolor: {
      default: '#007BFF',
      type: String
    },
    color: {
      default: '#000',
      type: String
    },
    fontsize: {
      default: 22,
      type: Number
    }
  }
}
</script>

<style lang="less" scoped>
.es-header-container {
  height: 50px;
  width: 100%;
  text-align: center;
  line-height: 50px;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
}
</style>
