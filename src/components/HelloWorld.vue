<template>
<div class="padding20">
  <div class="fs-18">Colors</div>
  <div class="text-dark fs-10">Brand color/Text color/Neutral color</div>
  <div class="fs-18 margint20">Brand color</div>
  <div class="background_list paddingv10" v-for="(item, index) in background" :key="index">
    <div class="flex-container-col center margint30" v-for="(itemB, indexB) in 9" :key="indexB">
      <div class="background" :class="'bg-'+item+'_'+itemB+'00'"></div>
      <div class="margint5 fs-12" v-text="'bg-'+item+'_'+itemB+'00'"></div>
    </div>
  </div>
</div>

</template>

<script>
function penson(name){
  this.name = name;
    console.log(this)
}
var p = new penson('this:::')
export default {
  name: 'HelloWorld',
  data () {
    return {
      background: ['red', 'yellow', 'blue', 'purple', 'green']
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.background_list{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));

  .background{
    width: 18px;
    height: 36px;
    border-radius: 28px;
  }
}
</style>
