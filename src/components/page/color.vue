<template>
<div>
  <div class="fs-18">颜色</div>
  <div class="text-dark fs-10">背景颜色/字体颜色/灰度字体颜色</div>
  <div class="fs-18 margint30">背景颜色</div>
  <div class="color_list">
    <div class="flex-container-col center margint30" v-for="(item, index) in colorText" :key="index">
      <div class="background" :class="'bg-'+item"></div>
      <div class="margint5 fs-12" v-text="'bg-'+item"></div>
    </div>
  </div>
  <div class="fs-18 margint30">字体颜色</div>
  <div class="color_list">
    <div class="flex-container-col center margint20" v-for="(item, index) in colorText" :key="index">
      <div class="margint5 fs-14 color" :class="'text-'+item" v-text="'text-'+item"></div>
    </div>
  </div>
   <div class="fs-18 margint30">灰度字体颜色</div>
  <div class="color_list">
    <div class="flex-container-col center margint20" v-for="(item, index) in grayText" :key="index">
      <div class="margint5 fs-14 color" :class="'text-'+item" v-text="'text-'+item"></div>
    </div>
  </div>
</div>
</template>
<script>
export default {
  name: 'color',
  data () {
    return {
      colorText: ['black', 'white', 'green', 'orange', 'red', 'yellow', 'blue', 'coffee', 'purple'],
      grayText: ['darker', 'dark', 'light', 'lighter']

    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.color_list{
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
