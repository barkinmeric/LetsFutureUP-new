<template>
    <section class="ments-sec">
      <h2>{{mentGrid.title}}</h2>
      <div class="grid-ctn">
        <img v-for="(ment, i) in mentGrid.elems" :key="i" :src="ment.imgSrc" alt="" class="ment-img">
      </div>
    </section>
</template>

<script>
export default {
  props:['mentGrid']
}
</script>

<style lang="scss" scope>
  .ments-sec {
    text-align: center;
    padding: 48px 14px 64px 14px;
    background: #F3F4F5;
    border-radius: 8px;
    .grid-ctn {
      margin-top: 38px;
      .ment-img {
        max-width: 287px;
        max-height: 260px;
        min-width: 287px;
        min-height: 260px;
        border-radius: 8px;
        margin: 10px;
      }
    }
  }
</style>