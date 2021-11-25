<template>
  <main >
    <section class="jumbo">
        <img src="../assets/img/jumbotron.jpg" alt="jumbotron">
    </section>
    
    <section class="archive">
      <div class="container">
        <div class="blue label">
          <h1>current series</h1>
        </div>
        <div class="sub-container">
        <ComicCard 
          v-for="(comic,index) in ComicData"
          :key="index"
          :thumb="comic.thumb"
          :series="comic.series"
         />
        </div>
      </div>
      <div class="container center">
        <button class="blue btn">
          <h3>load more</h3>
        </button>
      </div>
      
    </section>
    
  </main>
</template>

<script>

  import ComicCard from './ComicCard';
  import ComicData from '../assets/data/dc-comics.json';

  export default {
      name: 'Main',
      components:{
        ComicCard,
      },
      data(){
        return{
          ComicData,
        }
      }
  }
</script>

<style lang="scss" scoped>
  @import "../assets/style/mixins.scss";
  @import "../assets/style/generals.scss";
  @import "../assets/style/utilities.scss";
  @import "../assets/style/vars.scss";
  
  main{
    .jumbo{
      max-height: 400px;
      overflow: hidden;
      img{
        width: 100%;
      }
    }

    .archive{
      background-color: #1c1c1c;
      .container{
        .blue{
          display: inline-block;
          text-transform: uppercase;
          color: white;
          background-color: $primary-color-light;
        }
        .label{
          position: relative;
          transform: translate(0,-50%);
          padding: 15px 30px;          
        }
        &.center{
          @include center();
          button.btn{
            margin: 20px;
            padding: 15px 60px;
            border: 0;
          }
        }
        .sub-container{
          @include wrap();
          width:100%;
        }
      }

    }

  }
    
</style>