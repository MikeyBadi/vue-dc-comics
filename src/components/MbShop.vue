<template>
  <div class="container">

    <div class="merch">
      <ul v-for="(shop, index) in merch" :key="`merch-${index}`">
        <li>
          <img :src="'..'+'/assets/img/'+shop.img" :alt="shop.name">
          <a :href="shop.href">{{shop.name}}</a>
          </li>
      </ul>
    </div>

  </div>
</template>

<script>
export default {
  name: 'MbShop',
  data() {
    return {
      merch:[
        {
          img:'buy-comics-digital-comics.png',
          name:'DIGITAL COMICS',
          href:'#'
        },
        {
          img:'buy-comics-merchandise.png',
          name:'DC MERCHANDISE',
          href:'#'
        },
        {
          img:'buy-comics-subscriptions.png',
          name:'SUBSCRIPTION',
          href:'#'
        },
        {
          img:'buy-comics-shop-locator.png',
          name:'COMIC SHOP LOCATOR',
          href:'#'
        },
        {
          img:'buy-dc-power-visa.svg',
          name:'DC POWER VISA',
          href:'#'
        }
      ]
    }
  },
}
</script>

<style>

</style>

