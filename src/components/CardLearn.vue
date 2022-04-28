<template>
  <div>
      <div v-if=" thingToLearn.tipo  === 'flag'">
          <i class="fa-regular fa-flag  fa-5x"></i>
      </div>
       <div v-if=" thingToLearn.tipo  === 'gear'">
            <i class="fa-solid fa-gear  fa-5x"></i>
     </div>
    <div v-if=" thingToLearn.tipo  === 'ring'">
        <i class="fa-regular fa-life-ring  fa-5x"></i>
     </div>
    <div v-if=" thingToLearn.tipo  === 'display'">
        <i class="fa-solid fa-display  fa-5x"></i>
    </div>
      <h3>{{ thingToLearn.nomeArgomento }}</h3>
      <p>{{ thingToLearn.argomento }}</p>
  </div>
</template>

<script>
export default {
    name:'CardLearn',
    props:{
        thingToLearn:Object
    }
}
</script>

<style lang="scss" scoped>
div{
    font-size:1.1rem;
}
</style>