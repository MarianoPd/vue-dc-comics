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
  main{
    .jumbo{
      max-height: 400px;
      overflow: hidden;
    }

    .archive{
      background-color: #1c1c1c;
      .container{
        .sub-container{
          @include wrap();
          width:100%;
        }
      }

    }

  }
    
</style>