<template>
  <div>
          <h1>Learn At Your Own Pace!</h1>
          <h3>Get teamed up with people of the same will</h3>
          <ButtonComponent :message="message"/>
  </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
export default {
    name:'JumbotronComponent',
    data(){
        return{
            message: 'Get stareted for free'
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
}
</style>