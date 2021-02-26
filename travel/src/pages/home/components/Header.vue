<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont"> &#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
    <!-- <div class="home">This is Header</div> -->
  </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>
<style lang="stylus" scoped>
// @import '../../../assets/styles/varibles.styl'  正常按路径引入文件
// @import '~@/assets/styles/varibles.styl'   在vue中@代表的是src目录。
// ~styles/varibles.styl   这样写是因为  把build文件夹中 webpack.base.conf.js文件中 定义styles 指向src/assets/styles文件夹
@import '~styles/varibles.styl'

  .header
    line-height: .86rem
    display:flex
    color: #ffffff
    background: $bgColor
    .header-left
      width: .64rem
      float: left
      .back-icon
        font-size : .4rem
        text-align :center
    .header-input
      padding-left :.4rem
      color: #ccc
      flex: 1
      margin-top: .12rem
      margin-left: .2rem
      height:.64rem
      line-height:.64rem
      background: #ffffff
      border-radius: .1rem
    .header-right
      width: 1.24rem
      text-align: center
      float: right
      .arrow-icon
        font-size :.24rem
        margin-left :.04rem

</style>
