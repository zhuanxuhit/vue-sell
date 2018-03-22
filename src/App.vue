<template>
  <div id="app">
    <m-header :seller="seller"></m-header>
    <tab></tab>
    <router-view></router-view>
    <div class="content">
      I am content!
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
import MHeader from 'components/m-header/m-header'
import Tab from 'components/tab/tab'

const ERR_OK = 0

export default {
  data () {
    return {
      seller: {}
    }
  },
  created () {
    console.log(this.$http)
    this.$http.get('/api/seller').then((res) => {
      res = res.body
      if (res.errno === ERR_OK) {
        this.seller = res.data
      }
    })
  },
  components: {
    MHeader,
    Tab
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  /*#app*/
    /*.tab*/
      /*display: flex*/
      /*width: 100%*/
      /*height: 40px*/
      /*line-height: 40px*/
      /*.tab-item*/
        /*flex: 1*/
        /*text-align: center*/
</style>
