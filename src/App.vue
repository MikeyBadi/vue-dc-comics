<template>
  <div id="app">
    <!-- immetto i vari tag che ho usato -->
    <MbHeader/>

    <MbMain/>

    <MbShop/>
    <MbFooterLink/>
  </div>
</template>

<script>
// import nome dell'export che abbiamo dato from 'percorso del file'
import MbHeader from './components/MbHeader.vue';
import MbMain from './components/MbMain.vue';
import MbShop from './components/MbShop.vue';
import MbFooterLink from './components/MbFooterLink.vue';

export default {
  name: 'App',
  components: {
    // Solo in nome che abbiamo dato 
    MbHeader,
    MbMain,
    MbShop,
    MbFooterLink

  }
}
</script>

<style lang="scss">
  @import './assets/style/general';
  @import './assets/style/utils';
</style>
