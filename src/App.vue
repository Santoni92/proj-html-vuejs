<template>
  <div id="app">
    <HeaderComponent :vociMenuHeader="vociMenuHeader"/>
    <Jumbotron/>
    <MainComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import Jumbotron from './components/Jumbotron.vue'
import MainComponent from './components/MainComponent.vue'

export default {
  name: 'App',
  data(){
    return{
      vociMenuHeader:['Home','Pages','Courses','Features','Blog','Shop']
    }
  },
  components: {
    HeaderComponent,
    Jumbotron,
    MainComponent
  }
}
</script>

<style lang="scss">
*{
  padding:0;
  margin:0;
  box-sizing:border-box;
}
#app {
  
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;*/

}
</style>
