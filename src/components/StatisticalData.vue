<template>
  <div class="info-in-numeri">
      <div  v-for="(item,index) in  infoStatistiche" :key="index" >
        <span class="green">{{ item.informazioneNumero }}</span>
        <span>{{ item.informazioneSoggetto }}</span>
      </div>
  </div>
</template>

<script>
export default {
    name:'StatisticalData',
    props:{
        infoStatistiche:Array
    }
}
</script>

<style lang="scss" scoped>
 .info-in-numeri
 {
    display: flex;
    justify-content: space-evenly;
    div{
        display: flex;
        flex-direction: column;
        padding:40px;
        text-align:center;
        .green
         {
             color:#1fad96;
            font-size:30px;
            font-weight:800;
        }
    }
 }
</style>