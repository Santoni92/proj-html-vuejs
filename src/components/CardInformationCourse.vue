<template>
  <div>
      <div class="card">
          <div class="img">
               <img :src="informationCourse.urlImg" alt="">
          </div>
          <div class="costo-descrizione">
               <span class="green">{{ informationCourse.costo }}</span>
              <p>{{informationCourse.descrizione}}</p>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:'CardInformationCourse',
    props:{
        informationCourse:Object
    }
}
</script>

<style lang="scss" scoped>
.card{
    display:flex;
    font-weight:600;
    img{
         height: 200px;
         width: 200px;
        object-fit: cover;
        border-radius: 50%;
    }
    .costo-descrizione{
        padding:80px;
    }
    .green{
        color:#1fad96;
    }
}
</style>