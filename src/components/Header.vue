<template>
  <header >
    <div class="container ">
      <img src="../assets/img/dc-logo.png" alt="dc-logo">
    <ul>
      <li 
      v-for="(item,index) in links" :key="index"
      :class="{active: index === activeLink}"
      @click="activeLink = index">
        <a :href="item.url">
          {{item.text}}
        </a>
      </li>
      
    </ul>
    </div>
  </header>
</template>

<script>

export default {
  name: 'Header',
  data(){
    return{
      activeLink: 1,
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
  },
  
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/mixins.scss";
  @import "../assets/style/vars.scss";
  header{
    height: 120px;
    .container{
    @include center(between);
    height: 100%;
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
        &.active {
          border-bottom: 5px solid $primary-color-light;
        }
      }

    }
  }
  }

</style>