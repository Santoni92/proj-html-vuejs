<template>
  <div>
      <ul>
          <li v-for="(voceMenu,index) in vociMenu" :key="index">{{ voceMenu }}</li>
      </ul>
  </div>
</template>

<script>
export default {
    name:'CreateListComponent',
    props:{
        vociMenu:Array
    }
}
</script>

<style lang="scss" scoped>
ul{
    list-style-type:none;
}

</style>