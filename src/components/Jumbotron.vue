<template>
  <div>
          <h1>Learn At Your Own Pace!</h1>
          <h3>Get teamed up with people of the same will</h3>
          <ButtonComponent :messageButton="message"/>
          <div class="immagini">
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
    display:flex;
    flex-direction:column;
    align-items: center;
    color:white;
    background-color: #1f2154;
    h1,h3{
        margin-bottom:30px;
    }
    .immagini{
        display:flex;
        flex-direction:row;
        justify-content: center;
    }
}
</style>