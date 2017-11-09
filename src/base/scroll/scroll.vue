<template>
  <div ref="wrapper">
    <slot></slot>
  </div>
</template>

<script>
  import BScroll from 'better-scroll'
  export default {
    props: {
      probeType: {
        type: Number,
        default: 1
      },
      click: {
        type: Boolean,
        default: true
      },
      data: {
        type: Array,
        default: null
      }
    },
    mounted () {
      setTimeout(() => {
        this._intScroll()
      }, 20)
    },
    methods: {
      _intScroll: function () {
        if (!this.$refs.wrapper) {
          return
        }
        this.scroll = new BScroll(this.$refs.wrapper, {
          probeType: this.probeType,
          click: this.click
        })
      },
      enable: function () {
        this.scroll && this.scroll.enable()
      },
      disable: function () {
        this.scroll && this.scroll.disable()
      },
      refresh: function () {
        this.scroll && this.scroll.refresh()
      }
    },
    watch: {
      data () {
        setTimeout(() => {
          this.refresh()
        }, 20)
      }
    }
  }
</script>

<style lang="stylus" scoped>

</style>
