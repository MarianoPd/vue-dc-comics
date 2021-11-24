<template>
  <div id="app">
    <Header/>
    <Main/>
    <Merchandise/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Merchandise from './components/Merchandise.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Merchandise,
    Footer,
  }
}
</script>

<style lang="scss">
  @import "./assets/style/vars.scss";
  @import "./assets/style/utilities.scss";
  @import "./assets/style/generals.scss";
  @import "./assets/style/mixins.scss";
</style>
