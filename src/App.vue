<template>
  <Header> </Header>
  <InfiniteCarrousel> </InfiniteCarrousel>
  <Services> </Services> 
  <Footer>  </Footer>
</template>

<script>
import Header from './layout/Header.vue'
import Footer from './layout/Footer.vue';
import InfiniteCarrousel from './components/InfiniteCarrousel.vue';
import Services from './layout/Services.vue';


export default {
  name: 'App',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Header, Footer, InfiniteCarrousel, Services
  }
}
</script>

<style >
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  width: 100%;
  height: 100%;
  background-color: rgb(0, 0, 0);
}
</style>