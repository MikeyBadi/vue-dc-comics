<template>

  <header>

    <nav class="container">

      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="DC LOGO">
      </div>

      <div class="menu">
        <ul v-for="(el, index) in menu" :key="`menu-${index}`">
          <li>
            <a :href="el.href">{{el.text}}</a>
          </li>
        </ul>
      </div>

    </nav>

  </header>

</template>

<script>
export default {
  name: 'MbHeader',
  data() {
    return {
      menu:[
        {
          text: 'CHARACTERS',
          href: '#',
          active: false
        },
        {
          text: 'COMICS',
          href: '#',
          active: true
        },
        {
          text: 'MOVIES',
          href: '#',
          active: false
        },
        {
          text: 'TV',
          href: '#',
          active: false
        },
        {
          text: 'GAMES',
          href: '#',
          active: false
        },
        {
          text: 'COLLECTIBLES',
          href: '#',
          active: false
        },
        {
          text: 'VIDEOS',
          href: '#',
          active: false
        },
        {
          text: 'FANS',
          href: '#',
          active: false
        },
        {
          text: 'NEWS',
          href: '#',
          active: false
        },
        {
          text: 'SHOP',
          href: '#',
          active: false
        },
      ]
    }
  },

}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';
@import '../assets/style/vars';


header{
  height: 120px;
  nav{
    @include center();
    justify-content: space-between;
    height: 100%;

    .logo{
      width: 80px;
      img{
        width: 100%
      }
    }

    .menu{
      @include center();
      font-size: 12px;
      width: 60%;
      height: 100%;
      justify-content: space-between;
      ul{
        display: flex;
        a{
          color: black;
          padding-bottom: 52.5px;
          &:hover{
            border-bottom: 5px solid #3080F6;
            color: #3080F6;
          }
        }
      }
    }
  }
}

</style>