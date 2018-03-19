<template>
  <div class="tab">
    <!--<router-link tag="div" class="tab-item" to="/goods">-->
    <!--<span class="tab-link">商品</span>-->
    <!--</router-link>-->
    <div class="tab-item">
      <router-link to="/goods">商品</router-link>
    </div>
    <div class="tab-item">
      <router-link to="/ratings">评论</router-link>
    </div>
    <div class="tab-item">
      <router-link to="/seller">商家</router-link>
    </div>
    <!--<router-link tag="div" class="tab-item" to="/ratings">-->
      <!--<span class="tab-link">评论</span>-->
    <!--</router-link>-->
  </div>
</template>

<script type="text/ecmascript-6">
export default {}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/variable"
  .tab
    display: flex
    height: 40px
    line-height: 40px
    .tab-item
      flex: 1
      text-align: center
      & > a
        display : block
        font-size: 14px
        color: rgb(77, 85, 93)
        &.router-link-active
          color: rgb(240, 20, 20)
</style>
