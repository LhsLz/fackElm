<template>
  <span class="iconsize" :class="classMap[type]"></span>
</template>

<script>
export default {
  props: {
    type: Number,
    size: Number
  },
  data () {
    return {
      icon1: false,
      icon2: false
    }
  },
  methods: {
    whichsize () {
      if (this.size === 2) {
        icon2 = true
      } else if (this.size === 1) {
        icon1 = true
      }
    }
  },
  created () {
    this.classMap = ['decrease', 'discount', 'special', 'invoice', 'guarantee']
  }
}
</script>

<style lang="stylus">
  .icon1
         display inline-block
         vertical-align top
         width 12px
         height 12px
         margin-right 4px
         background-size 12px 12px
         background-repeat no-repeat
         &.decrease
           bg-image('decrease_1')
         &.discount
           bg-image('discount_1')
         &.guarantee
           bg-image('guarantee_1')
         &.invoice
           bg-image('invoice_1')
         &.special
           bg-image('special_1')
  .icon2
         display inline-block
         width 16px
         height 16px
         vertical-align top
         margin-right 6px
         background-size 16px 16px
         background-repeat no-repeat
         &.decrease
           bg-image('decrease_2')
         &.discount
           bg-image('discount_2')
         &.guarantee
           bg-image('guarantee_2')
         &.invoice
           bg-image('invoice_2')
         &.special
           bg-image('special_2')
</style>
