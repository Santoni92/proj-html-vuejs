<template>
  <div>
      <img :src="informationBlog.urlImg" alt="">
      <h3>{{ informationBlog.ruolo }}</h3>
      <p>{{ informationBlog.argument }}</p>
      <span>{{ informationBlog.date }}</span>
      <span>{{ informationBlog.views }}</span>
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

<style>

</style>