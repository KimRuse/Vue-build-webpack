<template>
  <div class="global-nav">
    <div class="contain">
      <Header />
      <Footer />
    </div>
  </div> 
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'GlobalNav',
  components: {
    Header, Footer
  }
}
</script>

<style lang="scss" scoped>
  @media screen and (min-width: 768px) {
    .contain {
      width: 750px;
      margin: 0 auto;
    }
  }
  .global-nav {
    border-top: 3px solid #009a61;
    box-shadow: 0px 2px 10px 0px rgba(0,0,0,0.1), 0 1px rgba(0,0,0,0.1);
    background: #fafafa;
  }
</style>
