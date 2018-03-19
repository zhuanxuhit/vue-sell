<template>
  <div id="app">
    <m-header></m-header>
    <tab></tab>
    <router-view></router-view>
    <div class="content">
      I am content!
    </div>
  </div>
</template>

<script>
import MHeader from 'components/m-header/m-header'
import Tab from 'components/tab/tab'
export default {
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
