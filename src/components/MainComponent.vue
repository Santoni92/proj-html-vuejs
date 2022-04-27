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
            <ButtonComponent :messageButton="message"/>
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
export default {
name:'MainComponent',

data(){
    return{
        testimonianze:[{
            opinione:'Let passion and determination be the guide along the way and develop at your own pace that\'s comfortable',
            nomeTestimone:'FANNIE MORENO',
            ruolo:'/FOUNDER & CEO'
            },
            {
                opinione:'I free to learn at my own pace, follow my own schedule and chose the subject i like.Great study portal for people like me.',
                nomeTestimone:'MINA HOLLACE',
                ruolo:'Freelancer'
            }
        ],
        infoStatistiche:[   //array di oggetti
            {
                informazioneNumero:'1.926',
                informazioneSoggetto:'FINISHED SESSIONS'
            },
            {
                informazioneNumero:'3.092+',
                informazioneSoggetto:'ENROLLED LEARNERS'
            },
            {
                informazioneNumero:'200',
                informazioneSoggetto:'ONLINE INSTRUCTORS'
            },
            {
                informazioneNumero:'100%',
                informazioneSoggetto:'SATISFACTION RATE'
            }
        ],
        cardImgInformations:[   //array di oggetti
            {
                titolo:'Graphic Design',
                testo:'Have a passion for graphics and art? Show your talents with confidence and self assertiveness',
                imgUrl:'img/home-6-service-image-01.png',
                imgPosition:'down'
            },
             {
                titolo:'business-administration',
                testo:'Learners are encouraged to study the mechanism and structure of system administratio',
                imgUrl:'img/home-6-service-image-02.png',
                imgPosition:'down'
            },
            {
                titolo:'Idea Discussion',
                testo:'Get teamed up with the specialist who work and teach coding for years at famous university',
                imgUrl:'img/home-6-service-image-03.png'
            },
            {
                titolo:'Web Development',
                testo:'Get teamed up with the specialist who work and teach coding for years at famous university',
                imgUrl:'img/home-6-service-image-04.png'
            }
        ],
        checklistInformations:{
                titolo:'SERVICES WE CAN PROVIDE FOR MY CLIENTS',
                titoletto:'TOGETHER WE CAN CREATE',
                checkItems:['Select and customize courses to your preferences','Change the tutor and make arrangements','Partecipate in events to join others','Get the desired certificate delivered at house']
            },
            informationCourses:[
                {
                    urlImg:'img/course-02-480x298.jpg',
                    costo:'$40.00',
                    descrizione:'Learning to write as a professional author',
                },
                {
                    urlImg:'img/stock-full-hd-03-480x298.jpg',
                    costo:'FREE',
                    descrizione:'Customer-centric info-tech Strategies'
                },
                {
                    urlImg:'img/stock-full-hd-04-480x298.jpg',
                    costo:'$19.00',
                    descrizione:'Open Programming Courses for Everyone:Python'
                },
                {
                    urlImg:'img/stock-full-hd-06-480x298.jpg',
                    costo:'$26.00',
                    descrizione:'Academic Listening and NoteTaking'
                },
                {
                    urlImg:'img/course-featured-image-01-480x298.jpg',
                    costo:'$39.00',
                    descrizione:'Master JQUERY ina short period of time'
                },
                {
                    urlImg:'img/stock-full-hd-05-480x298.jpg',
                    costo:'$59.00',
                    descrizione:'Introduction to JavaScript for Beginners'
                }
            ],
        message:'Get started for free'
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