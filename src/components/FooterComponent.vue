<template>
  <footer class="container d-flex justify-content-between">
      <div class="address">
          <h3>Adress</h3>
          <CreateListComponent :vociMenu="address[0]"/>
          <div>
              <i class="fa-brands fa-facebook"></i>
              <i class="fa-brands fa-twitter"></i>
              <i class="fa-brands fa-instagram"></i>
              <i class="fa-brands fa-linkedin"></i>
          </div>
      </div>
      <div class="d-flex justify-content-between explore-information">
          <div class="p-30">
              <h3>Explore</h3>
              <CreateListComponent :vociMenu="address[1]"/>
          </div>
            <CreateListComponent :vociMenu="address[2]" class="d-flex align-items-center"/>
          <div class="p-30">
             <h3>Information</h3>
             <CreateListComponent :vociMenu="address[3]"/>
            </div>
      </div>
  </footer>
</template>

<script>
import CreateListComponent from './CreateListComponent.vue'
//Strutture Dati
import address from '@/assets/address'
export default {
    name:'FooterComponent',
    data(){
        return {
            address
        }
    },
    components:{
        CreateListComponent
    }
}
</script>

<style lang="scss" scoped>
footer{
     background-color: #f5f7fa;
     padding:80px;
     .address{
         padding:20px;
     }
     .explore.information{
         flex-grow:1;
     }
     i{
         margin-right:20px;
     }
}

</style>