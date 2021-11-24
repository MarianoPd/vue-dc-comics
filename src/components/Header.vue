<template>
  <header class="container ">
    <img src="../assets/img/dc-logo.png" alt="">
    <ul>
      <li v-for="(item,index) in links" :key="index">
        <a :class="{active: item.current}" :href="item.url">{{item.text}}</a>
      </li>
      
    </ul>
  </header>
</template>

<script>

export default {
  name: 'Header',
  data(){
    return{
      links:[
        {
          url:'#',
          text: 'characters',
          current: false
        },
        {
          url:'#',
          text: 'comics',
          current: true
        },
        {
          url:'#',
          text: 'movies',
          current: false
        },
        {
          url:'#',
          text: 'tv',
          current: false
        },
        {
          url:'#',
          text: 'games',
          current: false
        },
        {
          url:'#',
          text: 'collectibles',
          current: false
        },
        {
          url:'#',
          text: 'videos',
          current: false
        },
        {
          url:'#',
          text: 'fans',
          current: false
        },
        {
          url:'#',
          text: 'news',
          current: false
        },
        {
          url:'#',
          text: 'shop',
          current: false
        },
    ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/mixins.scss";
  @import "../assets/style/vars.scss";
  header{
    @include center(between);
    height: 120px;
    img{
      width: 80px;
    }
    ul{
      @include orizontal();
      height: 100%;
      li{
        margin: 0 15px;
        text-transform: uppercase;
        font-weight: 600;
        height: 100%;
        @include center(align);
        
        &:hover,
        &.active{
          border-bottom: 5px solid $primary-color-light;
        }
      }

    }
  }

</style>