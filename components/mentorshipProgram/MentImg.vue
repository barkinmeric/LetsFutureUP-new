<template>
<div id="sec-single-img" :style="{ backgroundImage: `url(${require('@/static/pages/mentorshipProgram/' + img)})` }"></div>
</template>

<script>
export default {
  props: ['img']
}
</script>

<style lang="scss" scope>
  #secSingleImg {
    width: 287px;
    height: 260px;
    margin: 10px;
  }
</style>