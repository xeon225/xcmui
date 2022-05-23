<template>
<div class="paddingh20">
  <Color class="paddingv30 borderb"></Color>
  <Font class="paddingv30 borderb"></Font>
</div>

</template>

<script>
import Color from '@/components/page/color.vue'
import Font from '@/components/page/font.vue'
export default {
  name: 'index',
  components: {
    Color,
    Font
  },
  data () {
    return {
      // background: ['red', 'yellow', 'blue', 'purple', 'green']
    }
  }
}
</script>
<style lang="scss">
h1{
  font-size:20px;
  font-weight:normal;
}
</style>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
