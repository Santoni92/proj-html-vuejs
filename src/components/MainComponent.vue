<template>
<div class="container">
    <!--sez. let-passion-->
    <div id="let-passion">
        <Testimony :testimonianza="testimonianze[0]"/>
        <div>
                <StatisticalData :infoStatistiche="infoStatistiche"/>
        </div>
    </div>

    <!--sez. services-we-can-->
    <div id="services-we-can">
        <div class="card-side">
            <div v-for="(item,index) in cardImgInformations" :key="index" class="w-50">
                <CardImage :cardImgInformation = "item"/>
            </div>
        </div>
        <div>
            <ChecklistComponent :checklistInformations="checklistInformations"/>
            <ButtonComponent :messageButton="messageButtonInsert[0]"/>
        </div>
    </div>

    <!--sez. latest-featured-->
    <div id="latest-featured">
        <h3>CHOSE A COURSE TO GET STARTED</h3>
        <h1>Latest Featured Courses</h1>
        <div class="card-info-course">
            <div v-for="(informationCourse,index) in informationCourses" :key="index" class="w-50">
                <CardInformationCourse :informationCourse="informationCourse"/>
             </div>
        </div>
        <ButtonComponent :messageButton="messageButtonInsert[1]"/>
    </div>
    <!--sez. talk-about-->
    <div id="talk-about">
         <h1>Why People Talk About MaxCoach</h1>
         <div class="d-flex align-items-center">
            <img src="/img/testimonial-avata-02.jpg" alt="">
            <Testimony :testimonianza="testimonianze[1]"/>
         </div>
         <LogoBar :urlImgLogos="urlImgLogos"/>
    </div>
</div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
import Testimony from './Testimony.vue'
import StatisticalData from './StatisticalData.vue'
import CardImage from './CardImage.vue'
import ChecklistComponent from './ChecklistComponent.vue'
import CardInformationCourse from './CardInformationCourse.vue'
import LogoBar from './LogoBar.vue'
//Strutture Dati
import testimonianze from '@/assets/testimonianze'
import infoStatistiche from '@/assets/infoStatistiche'
import cardImgInformations from '@/assets/cardImgInformations'
import checklistInformations from '@/assets/checklistInformations'
import informationCourses from '@/assets/informationCourses'
import messageButtonInsert from '@/assets/messageButtonInsert'
import urlImgLogos from '@/assets/urlImgLogos'
export default {
name:'MainComponent',

data(){
    return{
        testimonianze,
        infoStatistiche,
        cardImgInformations,
        checklistInformations,
        informationCourses,
        messageButtonInsert,
        urlImgLogos
    }
},

 components:{
     ButtonComponent,
     Testimony,
     StatisticalData,
     CardImage,
     ChecklistComponent,
     CardInformationCourse,
     LogoBar
 }
}
</script>

<style lang="scss" scoped>
.container
{
    max-width:1170px;
    margin:0 auto;
    /*sez.let-passion*/
    #let-passion
    {display:flex;
     flex-direction:column;
     align-items: center;
     margin-top:50px;
     background-image:url('../../public/img/background-pattern-grid-line.png');
    }
    /*sez.services-we-can */
    #services-we-can
    {background-image:url('../../public/img/background-pattern-grid-line.png');
     display: flex;
     margin-top: 50px;
    .card-side{
        width:50%;
        display:flex;
        flex-wrap:wrap;
        align-items: baseline;
      }
    }
    /*sez.latest-featured*/
    #latest-featured{
        background-color: #f5f7fa;
        padding:80px;
        margin-top:50px;
        text-align:center;
        .card-info-course{
            display: flex;
            flex-wrap:wrap;
        }
    }
    /*sez. talk-about*/
    #talk-about{
       margin-top:50px;
        h1{
            text-align:center;
            margin-bottom:30px;
        }
        img{
            height: 250px;
            width: 250px;
            object-fit: cover;
            border-radius: 50%;
        }
    }
}
</style>