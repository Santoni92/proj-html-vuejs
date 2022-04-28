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
    <h1>Why People Talk About MaxCoach</h1>
    
</div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
import Testimony from './Testimony.vue'
import StatisticalData from './StatisticalData.vue'
import CardImage from './CardImage.vue'
import ChecklistComponent from './ChecklistComponent.vue'
import CardInformationCourse from './CardInformationCourse.vue'
//data
import testimonianze from '@/assets/testimonianze'
import infoStatistiche from '@/assets/infoStatistiche'
import cardImgInformations from '@/assets/cardImgInformations'
import checklistInformations from '@/assets/checklistInformations'
import informationCourses from '@/assets/informationCourses'
import messageButtonInsert from '@/assets/messageButtonInsert'
export default {
name:'MainComponent',

data(){
    return{
        testimonianze,
        infoStatistiche,
        cardImgInformations,
        checklistInformations,
        informationCourses,
        messageButtonInsert
    }
},

 components:{
     ButtonComponent,
     Testimony,
     StatisticalData,
     CardImage,
     ChecklistComponent,
     CardInformationCourse
 }
}
</script>

<style lang="scss" scoped>
.container
{
    /*general */
    .w-50{
    width:50%;
    }
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
        margin-top:50px;
        text-align:center;
        .card-info-course{
            display: flex;
            flex-wrap:wrap;
        }
    }
}
</style>