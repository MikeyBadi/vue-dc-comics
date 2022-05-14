<template>
  <div class="signUp">
    <div class="container">
      <button> SIGN-UP NOW!</button>
      <div class="social">
        <h3>FOLLOW US</h3>
        <img 
        v-for="(soc,index) in social" :key="`social-${index}`"
        :src="soc" alt="">
      </div>
    </div>
  </div>
</template>

<script>
  import first from '../assets/img/footer-facebook.png'
  import second from '../assets/img/footer-twitter.png'
  import third from '../assets/img/footer-youtube.png'
  import forth from '../assets/img/footer-pinterest.png'
  import fifth from'../assets/img/footer-periscope.png'
export default {
  name: 'MbSignUp',
  data() {
    return {
      social:[
        first,second,third,forth,fifth
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
  @import '../assets/style/mixins';
  @import '../assets/style/vars';

  .signUp{
    background-color: #303030;
  }
  button{
    background-color: transparent;
    border: 2px solid #358DFF;
    color: $primary-color;
    padding: 15px;
    font-size: 16px;
  }

  .container{
    @include center();
    justify-content: space-between;
    height: 110px;
  }

  .social{
    @include center();
    img{
      margin-left: 20px;
    }
    h3{
      margin-right: 15px;
      color: #358DFF;
    }
  }

</style>