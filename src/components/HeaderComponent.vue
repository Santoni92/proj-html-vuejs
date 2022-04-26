<template>
  <div class="container">
    <ul>
      <li v-for="voceMenu in vociMenuHeader" :key="voceMenu">
        {{ voceMenu }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent',
  props: {
    vociMenuHeader:Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
  max-width:1170px;
  margin:0 auto;
  display:flex;
  ul {
    display: flex;
    list-style-type: none;
    li{
      padding:5px;
    }
  }
}
</style>
