<template>
  <div class="card">
      <h2>{{ informationObject.titolo }}</h2>
      <p>{{ informationObject.testo }}</p>
      <img :src="informationObject.imgUrl" alt="">
  </div>
</template>

<script>
export default {
    name:'CardImgDown',
    props:{
        informationObject:Array
    },
}
</script>

<style>

</style>