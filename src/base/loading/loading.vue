<template>
    <div class="loading">
        <img src="./loading.gif" alt="" width="24" height="24">
        <p class="desc">{{title}}</p>
    </div>
</template>
<script tpye="text/ecmascript-6">
  export default {
    props: {
      title: {
        type: String,
        default: 'Loading'
      }
    }
  }
</script>
<style lang="stylus" scoped>
  @import "~common/stylus/variable"

  .loading
    width 100%
    text-align center
    .desc
      line-height 20px
      font-size: $font-size-small
      color $color-text-l
</style>
