<template>
  <div class="es-footer-container">
    <!-- 全选区域 -->
    <div class="custom-control custom-checkbox">
      <input type="checkbox" class="custom-control-input" id="fullCheck" />
      <label class="custom-control-label" for="fullCheck">全选</label>
    </div>
    <!-- 合计 -->
    <div>
      <span>合计</span>
      <span class="amount">￥0.00</span>
    </div>

    <button type="button" class="btn btn-primary btn-settle">结算（0）</button>
  </div>
</template>

<script>
export default {
  name: 'EsFooter'
}
</script>

<style lang="less" scoped>
.es-footer-container {
  position: fixed;
  left: 0;
  bottom: 0;
  height: 50px;
  width: 100%;
  // line-height: 50px;
  // text-align: center;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 10px;
  background-color: white;
  border-top: 1px solid #efefef;
  .amount{
    font-weight: 800;
    color:red;
  }
  .btn-settle{
    min-width: 90px;
    height: 38px;
    border-radius: 19px;
  }
}
</style>
