<template>
<div class="paddingh20">
  <div class="pos-f">
    <div class="flex-container nav-list">
      <a class="bg-white" href="#color">颜色</a>
      <a class="bg-white" href="#font">文字段落</a>
      <a class="bg-white" href="#badge">标识</a>
    </div>
  </div>
  <Color id="color" class="paddingv30 borderb"></Color>
  <Font id="font" class="paddingv30 borderb"></Font>
  <Badge id="badge" class="paddingv30 borderb"></Badge>
</div>

</template>

<script>
import Color from '@/components/page/color.vue'
import Font from '@/components/page/font.vue'
import Badge from '@/components/page/badge.vue'
export default {
  name: 'index',
  components: {
    Color,
    Font,
    Badge
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
.nav-list{
  a{
    padding:10px;
    color:#333;
  }
}
</style>
