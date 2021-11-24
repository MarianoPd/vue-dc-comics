<template>
  <section >
    <div class="container">
      <ul>
        <li v-for="(item,index) in links" :key="index">
          <img :src="item.image" alt="">
          <a :href="item.image">{{item.text}}</a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>

export default {
    name: 'Merchandise',
    data(){
      return{
        links:[
          {
            link: '#',
            image: require("../assets/img/buy-comics-digital-comics.png"),
            text: 'digital comics',
            current: false,
          },
          {
            link: '#',
            image: require('../assets/img/buy-comics-merchandise.png'),
            text: 'dc merchandise',
            current: false,
          },
          {
            link: '#',
            image: require('../assets/img/buy-comics-subscriptions.png'),
            text: 'subscription',
            current: false,
          },
          {
            link: '#',
            image: require('../assets/img/buy-comics-shop-locator.png'),
            text: 'comic shop locator',
            current: false,
          },
          {
            link: '#',
            image: require('../assets/img/buy-dc-power-visa.svg'),
            text: 'dc power visa',
            current: false,
          },
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/mixins.scss";
  @import "../assets/style/vars.scss";
  section{
    background-color: $primary-color-light;

    .container{    
    color: white;
    height: 155px;
    ul{
      @include center(between);
      @include orizontal();
      height: 100%;
      li{
        @include center(align);
        font-size: 15px;
        width: calc(100% / 5);
        img{
          max-width: 50px;
          max-height: 50px;
        }
        a{
          padding-left: 1rem;
          color: white;
          text-transform: uppercase;
        }
      }
    }
  }
  }
</style>