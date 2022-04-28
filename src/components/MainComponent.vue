<template>
<div class="container">

    <!--sez. let-passion-->
    <div id="let-passion" class="d-flex flex-direction-column align-items-center">
        <Testimony :testimonianza="testimonianze[0]"/>
        <div>
                <StatisticalData :infoStatistiche="infoStatistiche"/>
        </div>
    </div>

    <!--sez. services-we-can-->
    <div id="services-we-can" class="d-flex">
        <div class="card-side d-flex">
            <div v-for="(item,index) in cardImgInformations" :key="index" class="w-50">
                <CardImage :cardImgInformation = "item"/>
            </div>
        </div>
        <div class="d-flex flex-direction-column justify-content-center p-30">
            <ChecklistComponent :checklistInformations="checklistInformations"/>
            <ButtonComponent :messageButton="messageButtonInsert[0]" class="w-50-percento"/>
        </div>
    </div>

    <!--sez. latest-featured-->
    <div id="latest-featured">
        <h3>CHOSE A COURSE TO GET STARTED</h3>
        <h1>Latest Featured <span class="green">Courses</span></h1>
        <div class="card-info-course">
            <div v-for="(informationCourse,index) in informationCourses" :key="index" class="w-50 p-10">
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

    <!--sez. our-blogs--->
    <div id="our-blogs">
        <h3>ENJOY READING ON MAXCOACH</h3>
        <h1>Latest On <span class="green">Our Blogs</span> </h1>
        <div class="d-flex">
            <div v-for="(informationBlog,index) in informationsBlog" :key="index" class="w-33 p-10">
                <CardBlog :informationBlog="informationBlog"/>
            </div>
        </div>
    </div>

    <!--sez. help-you-learn-->
    <div id="help-you-learn">
        <h3>WANNA TRANSFORM YOUR LIFE?</h3>
        <h1>Glad to <span class="green">Help You</span> Learn</h1>
        <div class="d-flex align-items-center">
            <div v-for="(thingToLearn,index) in thingsToLearn" :key="index" class="w-25 p-10">
                <CardLearn :thingToLearn="thingToLearn"/>
            </div>
        </div>
        <div class="sfondo"></div>
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
import CardBlog from './CardBlog.vue'
import CardLearn from './CardLearn.vue'
//Strutture Dati
import testimonianze from '@/assets/testimonianze'
import infoStatistiche from '@/assets/infoStatistiche'
import cardImgInformations from '@/assets/cardImgInformations'
import checklistInformations from '@/assets/checklistInformations'
import informationCourses from '@/assets/informationCourses'
import messageButtonInsert from '@/assets/messageButtonInsert'
import urlImgLogos from '@/assets/urlImgLogos'
import informationsBlog from '@/assets/informationsBlog'
import thingsToLearn from '@/assets/thingsToLearn'
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
        urlImgLogos,
        informationsBlog,
        thingsToLearn
    }
},

 components:{
     ButtonComponent,
     Testimony,
     StatisticalData,
     CardImage,
     ChecklistComponent,
     CardInformationCourse,
     LogoBar,
     CardBlog,
     CardLearn
 }
}
</script>

<style lang="scss" scoped>
    /*sez.let-passion*/
    #let-passion
    {
     margin-top:50px;
     background-image:url('../../public/img/background-pattern-grid-line.png');
    }
    /*sez.services-we-can */
    #services-we-can
    {background-image:url('../../public/img/background-pattern-grid-line.png');
     margin-top: 50px;
    .card-side{
        width:50%;
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
    /*sez. our-blogs */
    #our-blogs{
         margin-top:50px;
         background-color: #f5f7fa;
         margin-top:50px;
         padding:20px 100px;
        h1,h3{
            text-align:center;
        }
    }
    /*sez. help-you-learn*/
    #help-you-learn{
         background-color: #f5f7fa;
         margin-top:50px;
         padding:100px;
         text-align: center;
         h1,h3{
             margin-bottom:30px;
         }
         .sfondo{
              padding:200px;
              background-image: url('../../public/img/home-6-services-image-1024x411.png');
              background-size: contain;
              background-position: center;
              background-repeat: no-repeat;
         }
    }

</style>