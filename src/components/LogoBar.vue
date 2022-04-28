<template>
  <div class="d-flex  justify-content-between align-items-center">
      <div v-for="(urlImgLogo,index) in  urlImgLogos" :key="index">
          <img :src="urlImgLogo" alt="">
      </div>
  </div>
</template>

<script>
export default {
    name:'LogoBar',
    props:{
        urlImgLogos:Array
    }
}
</script>

<style>

</style>