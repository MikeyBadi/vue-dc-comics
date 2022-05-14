<template>
<div class="footerLinks">
  <div class="container">
    <footer>
      <div class="links">
        <ul
        v-for="(el, index) in links" :key="`links-${index}`">
          <li>
            <h3>{{el.linkTitle}}</h3>
          </li>
          <li 
          v-for="(li,index) in el.link" :key="`links-${index}`">
            <a :href="li.href">{{li.txt}}</a>
            </li>
        </ul>
      </div>
      <img src="../assets/img/dc-logo-bg.png" alt="">
    </footer>
  </div>
  <MbSignUp/>
</div>
</template>

<script>
import MbSignUp from './MbSignUp.vue'
export default {
  name: 'MbFooterLink',
  components:{
    MbSignUp,
  },
  data() {
    return {
      links:[
          {
          linkTitle: 'DC COMICS',
          link:[
            {
              txt: 'Characters',
              href: '#'
            },
            {
              txt: 'Comics',
              href: '#'
            },
            {
              txt: 'Movies',
              href: '#'
            },
            {
              txt: 'TV',
              href: '#'
            },
            {
              txt: 'Games',
              href: '#'
            },
            {
              txt: 'Videos',
              href: '#'
            },
            {
              txt: 'Characters',
              href: '#'
            },
          ]
        },
        {
          linkTitle: 'SHOP',
          link:[
            {
              txt: 'Shop DC',
              href: '#'
            },
            {
              txt: 'Shop DC Collectables',
              href: '#'
            },
          
          ]
        },
        {
          linkTitle: 'DC',
          link:[
            {
              txt: 'Terns of Use',
              href: '#'
            },
            {
              txt: 'Privacy policy (NEW)',
              href: '#'
            },
            {
              txt: 'Ad Choices',
              href: '#'
            },
            {
              txt: 'Advertising',
              href: '#'
            },
            {
              txt: 'Jobs',
              href: '#'
            },
            {
              txt: 'Subscriptions',
              href: '#'
            },
            {
              txt: 'Talent Workshops',
              href: '#'
            },
            {
              txt: 'CPSC Certificates',
              href: '#'
            },
            {
              txt: 'Ratings',
              href: '#'
            },
            {
              txt: 'Shop Help',
              href: '#'
            },
            {
              txt: 'Contact Us',
              href: '#'
            },
          ]
        },
        {
          linkTitle: 'SITES',
          link:[
            {
              txt: 'DC',
              href: '#'
            },
            {
              txt: 'MAD Magazines',
              href: '#'
            },
            {
              txt: 'DC Kids',
              href: '#'
            },
            {
              txt: 'DC Universe',
              href: '#'
            },
            {
              txt: 'DC Power Visa',
              href: '#'
            },
          ]
        },
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
  @import '../assets/style/mixins';
  @import '../assets/style/vars';
  footer{
    height: 370px;
    display: flex;
    justify-content: space-between;
    position: relative;
    overflow: hidden;
  }
  .footerLinks{
    background-image: url('../assets/img/footer-bg.jpg') ;
    background-size: cover;

    .links{
      width: 30%;
      display: flex;
      flex-wrap: wrap;
      flex-direction: column;
      margin-top: 40px;
      
      ul{
        display: inline-block;
        justify-self: center;
        padding-bottom: 20px;
        h3{
          display: inline-block;
          padding-bottom: 15px;
          color: $primary-color;
        }
        a{
          color:$footer-links;
          font-size: 12px;
        }
      }

    }
      img{
        height: 35rem;
        position: absolute;
        right: 0px;
        top: -25.5%;
      }
  }
</style>