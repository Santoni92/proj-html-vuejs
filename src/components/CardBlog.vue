<template>
  <div>
      <img :src="informationBlog.urlImg" alt="">
      <h3>{{ informationBlog.ruolo }}</h3>
      <p>{{ informationBlog.argument }}</p>
      <div class="d-flex">
          <div><i class="fa-solid fa-calendar"></i>{{ informationBlog.date }} </div>
          <div><i class="fa-solid fa-eye"></i>{{ informationBlog.views }}</div>
      </div>
  </div>
</template>

<script>
export default {
    name:'CardBlog',
    props:{
        informationBlog:Object
    }
}
</script>

<style lang="scss" scoped>
img{
    width:100%;
}
</style>