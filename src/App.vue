<template>
  <Header> </Header>
  <Banner></Banner>
  <InfiniteCarrousel> </InfiniteCarrousel>
  <About></About>
  <Services> </Services> 
  <Clients></Clients>
  <Contact></Contact>
  <Footer>  </Footer>
</template>

<script>
import Header from './layout/Header.vue'
import Footer from './layout/Footer.vue';
import InfiniteCarrousel from './components/InfiniteCarrousel.vue';
import Services from './layout/Services.vue';
import About from './layout/About.vue';
import Clients from './layout/Clients.vue';
import Contact from './layout/Contact.vue';
import Banner from './layout/Banner.vue';
import './assets/fonts/fonts.css';


export default {
  name: 'App',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Header, Footer, InfiniteCarrousel, Services, About, Clients, Contact, Banner
  }
}
</script>

<style >
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'FuturaDisplay', 'Montserrat';
}

html, body {
  width: 100%;
  height: 100%;
  background-color: rgb(0, 0, 0);
}
</style>