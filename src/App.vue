<template>
  <div id="app">
    <HeaderComponent :vociMenuHeader="vociMenuHeader"/>
    <Jumbotron/>
    <MainComponent/>
    <FooterComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import Jumbotron from './components/Jumbotron.vue'
import MainComponent from './components/MainComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
//Strutture Dati
import vociMenuHeader from '@/assets/struttureDati/vociMenuHeader'
export default {
  name: 'App',
  data(){
    return{
      vociMenuHeader
    }
  },
  components: {
    HeaderComponent,
    Jumbotron,
    MainComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
@import '@/assets/commonStyle';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

}
</style>
