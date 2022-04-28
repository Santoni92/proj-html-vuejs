<template>
  <div class="d-flex flex-direction-column align-items-center">
          <h1>Learn At Your Own Pace!</h1>
          <h3>Get teamed up with people of the same will</h3>
          <ButtonComponent :messageButton="message"/>
          <div class="d-flex justify-content-center immagini">
              <img src="../../public/img/home-6-hero-left-person.png" alt="">
              <img src="../../public/img/home-6-hero-poster-final.jpg" alt="">
              <img src="../../public/img/home-6-hero-right-person.png" alt="">
          </div>
  </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
export default {
    name:'JumbotronComponent',
    data(){
        return{
            message: 'Get started for free '
        }
    },
    components:{
        ButtonComponent
    }
}
</script>

<style lang="scss" scoped>
div{
    padding:50px;
    color:white;
    background-color: #1f2154;
    .immagini{
        margin-top:100px;
    }
    h1,h3{
        margin-bottom:30px;
    }
}
</style>