<template>
  <div id="app">
    <Header :links="linksLabel"/>
    <JumboBg/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import JumboBg from './components/JumboBg.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    JumboBg
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
      ]
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
