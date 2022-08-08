<template>
  <div id="depImg">
      <dep-single-img v-for="(img, i) in secImg" :key="i" :img="img"/>
  </div>
</template>

<script>
import DepSingleImg from './DepSingleImg.vue'
export default {
  components: { DepSingleImg },
  props: ['secImg']
}
</script>

<style lang="scss" scope>
  #depImg {
    width: 50%;
    padding: 0 20px 20px 20px 20px;
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
    @media (max-width: 1400px) {
        min-width: 650px;
		}
    @media (max-width: $mobile_bp) {
        min-width: 550px;
		}	
  }
</style>