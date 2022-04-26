<template>
  <div class="container">
    <img src="../../public/img/dark-logo.png" alt="">
    <div class="navbar">
       <ul>
          <li v-for="voceMenu in vociMenuHeader" :key="voceMenu">
            <div>{{ voceMenu }} <i class="fa-solid fa-chevron-down"></i></div>
          </li>
        </ul>
        <div class="icons">
          <div><i class="fa-solid fa-circle-user"></i></div>
           <div><i class="fa-solid fa-cart-shopping"></i></div>
        </div>
    </div>
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
  justify-content: space-between;
  align-items: center;
  .navbar{
    display:flex;
    justify-content: space-between;
    align-items: center;
    ul {
        display: flex;
        list-style-type: none;
        li{
            margin-right:30px;
          }
        }
        .icons{
          display:flex;
          justify-content:space-between;
        }

   }
}
</style>
