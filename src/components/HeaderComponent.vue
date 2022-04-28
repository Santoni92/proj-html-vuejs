<template>
<div>
  <div class="container d-flex justify-content-between align-items-center p-30">
    <img src="../../public/img/dark-logo.png" alt="">
    <div class=" d-flex justify-content-between align-items-center navbar">
       <ul class="d-flex">
          <li v-for="voceMenu in vociMenuHeader" :key="voceMenu">
            <div>{{ voceMenu }} <i class="fa-solid fa-chevron-down"></i></div>
          </li>
        </ul>
        <div class=" d-flex justify-content-between">
          <div class=p-10><i class="fa-solid fa-circle-user"></i></div>
           <div class=p-10><i class="fa-solid fa-cart-shopping"></i></div>
        </div>
        <div class="search">
          <input type="text" placeholder="Search..." class="p-10">
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
    color:white;
    img{
      width:20%;
    }
      ul {
          list-style-type: none;
          li{
             /*margin-right:30px;*/
             padding:10px;
            }
          }
          .search{
            background-color:white;
            border: 1px solid wheat;
            border-radius:10px;
            padding:5px;
           input{
                border-style: none;
               }
               i{
                 color:#1fad96;
               }
          }
}
</style>
