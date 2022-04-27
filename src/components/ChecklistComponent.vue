<template>
  <div class="check-information">
    <h3>{{ checklistInformations.titoletto }}</h3>
    <h1>{{ checklistInformations.titolo }}</h1>
    <ul>
      <li v-for="(checkItem,index) in checklistInformations.checkItems" :key="index"><i class="fa-solid fa-check"></i>{{ checkItem }}</li>
    </ul>
  </div>
</template>

<script>
export default {
    name:'ChecklistComponent',
    props:{
        checklistInformations:Object
    }
}
</script>

<style lang="scss" scoped>
div{
  h3,h1{
    margin-bottom:40px;
  }
   ul{
     list-style-type:none;
     li{
         margin-top:20px;
         margin-bottom: 20px;
     }
     li i{
         margin-right:20px;
         color:#1fad96;
     }
 }
}

</style>