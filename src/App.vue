<template>
  <div id="app">
    <HeaderComponent :vociMenuHeader="vociMenuHeader"/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'

export default {
  name: 'App',
  data(){
    return{
      vociMenuHeader:['Home','Pages','Courses','Features','Blog','Shop']
    }
  },
  components: {
    HeaderComponent
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;
  color: #2c3e50;
  margin-top: 60px;*/
}
</style>
