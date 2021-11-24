<template>
  <main >
    <div class="container">
      <h1>  --&gt; Content goes here&lt;--  </h1>
    </div>
  </main>
</template>

<script>
export default {
    name: 'Main',
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/mixins.scss";
  main{
    @include center(align);
    height: 135px;
    color: white;
    background-color: black;
    padding-left: 50px ;
  }
</style>