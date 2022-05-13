<template>
  <div class="shopping">
    <div class="container">

      <div class="merch">
        <ul>
          <li v-for="(shop, index) in merch" :key="`merch-${index}`">
            <img :src="shop.img" :alt="shop.name" :class="shop.class">
            <a :href="shop.href">{{shop.name}}</a>
            </li>
        </ul>
      </div>

    </div>
  </div>
</template>

<script>
  import first from '../assets/img/buy-comics-digital-comics.png'
  import second from '../assets/img/buy-comics-merchandise.png'
  import third from '../assets/img/buy-comics-subscriptions.png'
  import forth from '../assets/img/buy-comics-shop-locator.png'
  import fifth from'../assets/img/buy-dc-power-visa.svg'
export default {
  name: 'MbShop',
  data() {
    return {
      merch:[
        {
          img: first,
          name:'DIGITAL COMICS',
          href:'#',
          class:''
        },
        {
          img: second,
          name:'DC MERCHANDISE',
          href:'#',
          class:''
        },
        {
          img: third,
          name:'SUBSCRIPTION',
          href:'#',
          class:''
        },
        {
          img: forth,
          name:'COMIC SHOP LOCATOR',
          href:'#',
          class:''
        },
        {
          img: fifth,
          name:'DC POWER VISA',
          href:'#',
          class:'short'
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
  @import '../assets/style/mixins';
  @import '../assets/style/vars';

  .shopping{
    background-color: #3182F9;
    .merch{
      
      ul{
        @include center();
        justify-content: space-around;
        li{
          @include center();
          display: flex;
          margin: 50px;
          cursor: pointer;
          img{
            height: 50px;
            margin-right: 15px;
          }
          .short{
            height: 35px;
          }
          a{
            color: $primary-color;
            font-size: 14px;
            text-align: center;
          }
        }
      }
    }
  }
</style>