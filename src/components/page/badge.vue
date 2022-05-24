<template>
<div>
  <h1>标识</h1>
  <div class="text-dark fs-10">标识颜色/标识状态/标识组</div>
  <div class="fs-18 margint20">标识颜色</div>
  <div class="badge_list">
    <div class="flex-container-col center margint10" v-for="(item, index) in colorText" :key="index">
      <div class="badge" :class="'badge-'+item" v-text="item"></div>
      <div class="margint5 fs-12" v-text="'badge-'+item"></div>
    </div>
  </div>
  <div class="fs-18 margint20">标识状态</div>
  <div class="badge_list margint20" v-for="(itemT, indexT) in badgeType" :key="indexT">
    <div class="flex-container-col center margint10" v-for="(item, index) in colorText" :key="index">
      <div class="badge" :class="'badge-'+item+' badge-'+itemT" v-text="itemT"></div>
      <div class="margint10 fs-12" v-text="'badge-'+itemT"></div>
    </div>
  </div>
  <div class="fs-18 margint20">标识组</div>
  <div>
    <div class="badge-group margint20" v-for="(itemT, indexT) in badgeTrem" :key="indexT">
      <div class="badge badge-red" :class="'badge-'+itemT" v-for="(item, index) in 9" :key="index" v-text="item"></div>
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
      badgeType: ['pill', 'reverse', 'round', 'radius', 'flag'],
      badgeTrem: ['', 'reverse', 'round']
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.badge_list{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
  .badge-white{
    color:#666;
    border:1px solid #ccc;
  }
}
</style>
