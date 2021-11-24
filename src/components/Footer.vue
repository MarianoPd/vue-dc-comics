<template>
  <footer>
    <div>
      <section class="jumbo">
        <div class="container">
          <div class="sub-container left">
           <div class="list">
             <h1>dc comics</h1>
             <ul>
               <li>Charactrs</li>
               <li>Comics</li>
               <li>Movies</li>
               <li>TV</li>
               <li>Games</li>
               <li>Videos</li>
               <li>News</li>
             </ul>
           </div>
           <div class="list">
             <h1>shop</h1>
             <ul>
               <li>Shop DC</li>
               <li>Shop DC Collectables</li>
             </ul>
           </div>
           <div class="list">
             <h1>dc</h1>
             <ul>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
               <li>Terms Of Use</li>
             </ul>
           </div>
           <div class="list">
             <h1>sites</h1>
             <ul>
               <li>lorem</li>
               <li>lorem</li>
               <li>lorem</li>
               <li>lorem</li>
               <li>lorem</li>
             </ul>
           </div>
          </div>
          <div class="sub-container right">
            <img src="../assets/img/dc-logo-bg.png" alt=""> 
          </div>
        </div>
      </section>
      <section class="bottom">
        <div class="container">
          <button><h3>sign up now!</h3></button>
          <div class="socials">
            <h3>follow us</h3>
            <img src="../assets/img/footer-facebook.png" alt="">
            <img src="../assets/img/footer-twitter.png" alt="">
            <img src="../assets/img/footer-youtube.png" alt="">
            <img src="../assets/img/footer-pinterest.png" alt="">
            <img src="../assets/img/footer-periscope.png" alt="">
          </div>
        </div>
      </section>
    </div>
  </footer>
</template>

<script>

export default {
    name: 'Footer',
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/mixins.scss";
  @import "../assets/style/vars.scss";
  
  footer{

    & > div{
      width: 100%;
      
      section.jumbo{
        
        width: 100%;
        height: 370px;
        background-image: url('../assets/img/footer-bg.jpg');
        
        .container{
          height: 100%;
          @include center(align);
          .sub-container{
            height: 100%;
            width: 50%;
          }
          .left{
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            padding-top: 20px;
            .list{
              padding-top: 20px;
              width: 140px;
              h1{
                text-transform: uppercase;
                color: white;
                margin-bottom: 20px;
              }
              ul{
                color: #959595;
                font-size: 12px
              }
            }
          }
          .right{
            @include center();
            overflow: hidden;
          }
        }
      }
      section.bottom{
        width: 100%;
        height: 110px;
        background-color: #303030;
        .container{
          height: 100%;
          @include center(between);
          h3{
            text-transform: uppercase;
          }
          button{
            @include center();
            padding: 10px;
            border:2px solid $primary-color-dark;
            border-radius:0;
            background-color: #303030;
            color:white;
          }
          .socials{
            @include center(evenly);
            *{
              margin-right: 15px;
            }
            h3{
              color: $primary-color-dark;
              margin-right: 25px;
            }
          }
        }
      }
    }
  }
</style>