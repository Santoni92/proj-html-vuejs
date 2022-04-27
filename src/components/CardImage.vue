<template>
  <div class="card">
      <div v-if="cardImgInformation.imgPosition === 'down' ">
          <h2>{{ cardImgInformation.titolo }}</h2>
          <p>{{ cardImgInformation.testo }}</p>
          <img :src="cardImgInformation.imgUrl" alt="">
      </div>
      <div v-else>
          <img :src="cardImgInformation.imgUrl" alt="">
          <h2>{{ cardImgInformation.titolo }}</h2>
          <p>{{ cardImgInformation.testo }}</p>
      </div>
  </div>
</template>

<script>
export default {
    name:'CardImage',
    props:{
         cardImgInformation:Object
    },
}
</script>

<style lang="scss" scoped>
.card{
    background-color: #f6f3f6;
    border:1px solid white;
    border-radius:10px;
    padding:10px;
    h2,p{
        margin-bottom:20px;
    }
}
</style>