<template>
<div class="com-div">
  <div class="comics">
    <img :src="card.thumb" :alt="card.series">
  </div>
    <p>{{card.series}}</p>
</div>
</template>

<script>
export default {
 name: 'MbMainSeries',
   props:{
    card: Object
  },
}
</script>

<style lang="scss" scope>
.com-div{
  display: flex;
  flex-direction: column;
  flex-basis: calc(100vw / 9);
  max-width: calc(100vw / 9);
  height: calc(100vw / 9);
  margin: 10px 14px;
}
.comics{
  height: 180px;
 overflow: hidden;
 display: flex;
 img{
   width: 100%;
   height: 152%;
 }
}
</style>