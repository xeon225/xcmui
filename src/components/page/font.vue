<template>
<div>
  <h1>文字段落</h1>
  <div class="text-dark fs-10">字体大小/文本对齐/字体粗细/限制行数/行间距</div>
  <div class="fs-18 margint20">字体大小</div>
  <div class="text_list">
    <div class="text-center margint20" v-for="(item, index) in fsNum" :key="index">
      <div class="margint5" :class="'fs-'+(item+9)" v-text="'fs-'+(item+9)"></div>
    </div>
  </div>
  <div class="fs-18 margint30">文本对齐</div>
  <div>
    <div class="flex-container left margint20" v-for="(item, index) in alignment" :key="index">
      <div>
        <div class="fs-14" style="min-width:100px;" v-text="'text-'+item"></div>
        <div v-if="index < 3" class="fs-16 flex1 paddingv5" style="background:#eee " :class="'text-'+item">文字</div>
        <div v-else class="fs-16 flex1 paddingv5" style="background:#eee; overflow: hidden;" :class="'text-'+item">段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落</div>
      </div>
    </div>
  </div>
  <div class="fs-18 margint30">字体粗细</div>
  <div class="weight_list">
    <div class="text-center margint20" v-for="(item, index) in fsWeight" :key="index">
      <div class="margint5" :class="'text-weight'+(item*100)" v-text="'text-wieight'+(item*100)"></div>
    </div>
    <div class="text-center margint20">
      <div class="margint5 text-bolder" v-text="'text-bolder'"></div>
    </div>
  </div>
  <div class="fs-18 margint30">限制行数</div>
  <div>
    <div class="flex-container left margint20" v-for="(item, index) in limitNum" :key="index">
      <div class="fs-14" style="min-width:100px;" v-text="'text-limit'+item"></div>
      <div class="fs-16 flex1" style="background:#eee; overflow: hidden;" :class="'text-limit'+item">段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落 段落</div>
    </div>
  </div>
  <div>
    <div class="flex-container left margint20" v-for="(item, index) in limitNum" :key="index">
      <div class="fs-14" style="min-width:100px;" v-text="'text-fixed'+item"></div>
      <div class="fs-16 flex1" style="background:#eee; overflow: hidden;" :class="'text-fixed'+item">段落 段落 段落 段落 段落 段落 段落 段落 段落 段落</div>
    </div>
  </div>
  <div class="fs-18 margint30">行间距</div>
  <div>
    <div class="flex-container left margint20">
      <div class="fs-14" style="min-width:100px;">lh-1</div>
      <div class="fs-16 flex1 lh-1" style="background:#eee; overflow: hidden;">段落 段落 段落 段落 段落 段落 段落 段落 段落 段落</div>
    </div>
    <div class="flex-container left margint20" v-for="(item, index) in lineHeight" :key="index">
      <div class="fs-14" style="min-width:100px;" v-text="'lh-'+((item + 2) * 4)"></div>
      <div class="fs-16 flex1" style="background:#eee; overflow: hidden;" :class="'lh-'+((item + 2) * 4)">段落 段落 段落 段落 段落 段落 段落 段落 段落 段落</div>
    </div>
  </div>
  <div class="fs-18 margint30">标题线</div>
  <div class="margint20">
    <div class="lineTitle fs-16">标题标题标题标题</div>
  </div>
</div>
</template>
<script>
export default {
  name: 'color',
  data () {
    return {
      fsNum: 11,
      fsWeight: 9,
      limitNum: 4,
      lineHeight: 13,
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
}
.weight_list{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
}
</style>
