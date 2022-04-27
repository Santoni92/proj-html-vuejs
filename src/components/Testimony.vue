<template>
  <div>
      <p>{{ testimonianza.opinione }}</p>
      <span>{{ testimonianza.nomeTestimone }}</span>
      <span>{{ testimonianza.ruolo }}</span>
  </div>
</template>

<script>
export default {
    name:'TestimonyComponent',
    props:{
        testimonianza:Object
    }
}
</script>

<style lang="scss" scoped>
    div{
        display: flex;
        flex-direction: column;
        text-align:center;
         p{
            font-size:30px;
            }
     }
</style>