<template>
    <div id="ment-img">
      <ment-img v-for="(img, i) in secImg" :key="i" :img="img"/>
    </div>
</template>

<script>
import MentImg from './MentImg.vue'
export default {
  components: { MentImg }
//   props: ['secImg']
}
</script>

<style lang="scss" scope>
    #ment-img {
        padding: 14px;
    }
</style>