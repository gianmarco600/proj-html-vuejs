<template>
  <div id="app">
    <Header :logo="srcs.logoWhite" :links="linksLabel"/>
    <Jumbo/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Jumbo from './components/Jumbo.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Jumbo
  },
  data(){
    return{
      linksLabel:[
        'home',
        'pages',
        'courses',
        'features',
        'blog',
        'shop'
      ],
      srcs:{
                anteprimaVideo : '@/assets/img/home-6-hero-poster-final.jpg',
                logoWhite : '@/../public/imgs/light-logo.png'
            }
    }
  }
}
</script>

<style lang="scss">
@import '@/style/commons.scss';

#app {
  font-family: 'Quicksand' sans-serif;
}
</style>
