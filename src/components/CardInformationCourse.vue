<template>
  <div>
      <div class="card d-flex align-items-center justify-content-center">
          <div class="img">
               <img :src="informationCourse.urlImg" alt="">
          </div>
          <div class="costo-descrizione">
               <span class="green">{{ informationCourse.costo }}</span>
               <p>{{ informationCourse.descrizione }}</p>
               <div class="d-flex align-items-center justify-content-center">
                    <i class="fa-solid fa-rectangle-list"></i>{{ informationCourse.numeroLezioni }}
                    <i class="fa-solid fa-user"></i>{{ informationCourse.numeroStudenti }}
               </div>
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
    font-weight:600;
    img{
         height: 250px;
         width: 250px;
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