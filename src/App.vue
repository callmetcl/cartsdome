<template>
  <div class="app-container">
    <h1>App 跟组件</h1>
    <EsHeader></EsHeader>
    <EsFooter></EsFooter>
  </div>
</template>

<script>
import EsHeader from './components/EsHeader/EsHeader.vue'
import EsFooter from './components/EsFooter/EsFooter.vue'
export default {
  name: 'MyApp',
  created() {
    this.getGoodsList()
  },
  components: {
    EsHeader,EsFooter
  },
  data() {
    return {
      goodslist: []
    }
  },
  methods: {
    async getGoodsList() {
      const { data: res } = await this.$http.get('/api/cart')
      console.log(res)
      if (res.status !== 200) return alert('数据请求失败')
      this.goodslist = res.list
    }
  }
}
</script>

<style lang="less" scoped>
.app-container {
  padding-top: 50px 0;
}
</style>
