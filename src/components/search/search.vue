<template>
  <div>
    <button v-on:click="_initAn">123</button>
     <button v-on:click="greet">Greet</button>
  </div>
</template>

<script>
import snabbt from 'snabbt.js'
export default {
  data () {
    return {
      name: 'vue'
    }
  },
  methods: {
    _initAn: function (event) {
      snabbt(event.target, {
        position: [100, 0, 0],
        rotation: [Math.PI, 0, 0],
        easing: 'ease'
      })
    },
    greet: function (event) {
      alert('hellp' + this.name)
    }
  }
}
</script>
<style lang="stylus" scoped>
button
  display inline
  background-color white
  border-radius 4px
  color #555
  text-align center
  font-size 11px
  font-weight 600
  text-decoration none
  cursor pointer 
  border: 1px solid #bbbbbb
  height 38px
  line-height 38px
  padding 0 30px
  letter-spacing .1rem
  text-transform uppercase
  white-space nowrap
  box-sizing border-box
  margin-bottom 1rem
</style>