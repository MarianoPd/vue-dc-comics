<template>
  <div class="card">
      <div class="image">
          <img :src="thumb" :alt="series">
      </div>
      <p>{{series}}</p>
  </div>
</template>

<script>
export default {
    name: 'ComicCard',
    props:{
        thumb: String,
        series: String,
    }
}
</script>

<style lang="scss" scoped>
    @import "../assets/style/generals.scss";
    @import "../assets/style/mixins.scss";
    @import "../assets/style/utilities.scss";
    @import "../assets/style/vars.scss";

    .card{
        flex-basis: calc(100% / 6) ;
        padding: 15px;
        
        .image{
            width: 185px;
            height: 185px;
            overflow: hidden;
        }
        p{
            color: white;
            text-transform: uppercase;
            margin: 20px 0;
        }
    }
</style>