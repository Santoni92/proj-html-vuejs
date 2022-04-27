<template>
<div>
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
        <div class="search">
          <input type="text" placeholder="Search...">
          <i class="fa-solid fa-magnifying-glass"></i>
        </div>
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
div{
  background-color: #1f2154;
  .container{
    max-width:1170px;
    margin:0 auto;
    display:flex;
    justify-content: space-between;
    align-items: center;
    color:white;
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
            margin-right:30px;
          }
          .search{
            background-color:white;
            border: 1px solid wheat;
            border-radius:50px;
            padding:5px;
           input{
                border-style: none;
               }
               i{
                 color:#1fad96;
               }
          }
     }
  }
}
</style>
