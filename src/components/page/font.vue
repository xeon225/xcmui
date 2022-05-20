<template>
<div>
  <div class="fs-18">字体段落</div>
  <div class="text-dark fs-10">字体大小/文本对齐</div>
  <div class="fs-18 margint20">字体大小</div>
  <div class="text_list">
    <div class="text-center margint20" v-for="(item, index) in fsNum" :key="index">
      <div class="margint5" :class="'fs-'+(item+9)" v-text="'fs-'+(item+9)"></div>
    </div>
  </div>
   <div class="fs-18 margint30">文本对齐</div>
  <div class="">
    <div class="flex-container left margint20" v-for="(item, index) in alignment" :key="index">
      <div class="fs-14" style="min-width:100px;" v-text="'text-'+item"></div>
      <div v-if="index < 3" class="fs-16 flex1 paddingv5" style="background:#eee" :class="'text-'+item">文字</div>
      <div v-else class="fs-16 flex1 paddingv5" style="background:#eee; overflow: hidden;" :class="'text-'+item">段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落</div>
    </div>
  </div>
</div>
</template>
<script>
export default {
  name: 'color',
  data () {
    return {
      fsNum: 11,
      alignment: ['left', 'right', 'center', 'justify', 'nowrap', 'indent'],
      grayText: ['darker', 'dark', 'light', 'lighter']
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.text_list{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));

  .background{
    width: 18px;
    height: 36px;
    border-radius: 28px;
    &.bg-white{
      outline:1px solid #666;
    }
  }
  .color{
    &.text-white{
      text-shadow:0px 0px 2px #000;
    }
  }
}
</style>
