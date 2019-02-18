<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>输入城市/游玩/主题
    </div>
    <router-link to='/city'>
      <div class="header-right">
        {{this.city}}
        <span class="iconfont">&#xe62d;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default{
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    line-height:$headerHeight
    display: flex
    background: $bgColor
    color: #fff
    .header-left
      width: 0.64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height:0.64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      line-height: 0.64rem
      color: #ccc
    .header-right
      min-width: 1.04rem
      padding:0 .1rem
      float: right
      text-align: center
      color:#fff
      .arrow-icon
        font-size: .20rem
</style>
