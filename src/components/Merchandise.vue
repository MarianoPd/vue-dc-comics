<template>
  <section >
    <div class="container">
      <ul>
        <li v-for="(item,index) in links" :key="index">
          <img :src="item.image" alt="">
          <a :href="'../assets/img/' + item.image">{{item.text}}</a>
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
            image: "dc-logo.png",
            text: 'digital comics',
            current: false,
          },
          {
            link: '#',
            image: '../assets/img/buy-comics-digital-comics.png',
            text: 'dc merchandise',
            current: false,
          },
          {
            link: '#',
            image: '../assets/img/buy-comics-digital-comics.png',
            text: 'subscription',
            current: false,
          },
          {
            link: '#',
            image: '../assets/img/buy-comics-digital-comics.png',
            text: 'comic shop locator',
            current: false,
          },
          {
            link: '#',
            image: '../assets/img/buy-comics-digital-comics.png',
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
    height: 150px;
    ul{
      @include center(evenly);
      @include orizontal();
      height: 100%;
      li{
        a{
          color: white;
        text-transform: uppercase;
        }
      }
    }
  }
  }
</style>