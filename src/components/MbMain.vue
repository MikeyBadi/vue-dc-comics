<template>
    <main>

    <div class="container">
      <div class="current">
        <div>
          <h2>CURRENT SERIES</h2>
        </div>
      </div>

      <div>
        <div class="com-cont">
          <MbMainSeries
          v-for="(com,index) in json"
          :key="`comics-${index}`"
          :card="com"
        />
        </div>

        <div class="button-div">
          <button>LOAD MORE</button>
        </div>

      </div>

    </div>
    
  </main>
</template>

<script>
import MbMainSeries from './MbMainSeries.vue'
import dcJson from '../assets/data/dc-comics.json'
  export default {
    name: 'MbMain',
    components:{
      MbMainSeries
    },
    data() {
    return {
      json: dcJson
    }
    },
    props:{
      card: Object
    },
  }
</script>

<style lang="scss" scoped>

  @import '../assets/style/mixins';
  @import '../assets/style/vars';

  main{
    background-color: #1C1C1C;
    color: $primary-color;
    padding-top: 50px;
  }
  .current{
    position: absolute;
  }
  .current div{
    width: 236px;
    background-color: $dc-blue;
    padding: 15px 25px;
    position: relative;
    bottom: 80px;
    left: 0;
  }

  .com-cont{
    display: flex;
    flex-wrap: wrap;
  }
  .button-div{
    @include center();
    padding: 60px 0 20px;
    button{
      cursor: pointer;
      display: inline-block;
      padding: 10px 60px;
      border: 0px solid;
      color: $primary-color;
      background-color: $dc-blue;
    }
  }

</style>