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
    <h3>CHOSE A COURSE TO GET STARTED</h3>
</div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
import Testimony from './Testimony.vue'
import StatisticalData from './StatisticalData.vue'
import CardImage from './CardImage.vue'
import ChecklistComponent from './ChecklistComponent.vue'
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
        message:'Get started for free'
    }
},

 components:{
     ButtonComponent,
     Testimony,
     StatisticalData,
     CardImage,
     ChecklistComponent
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
     margin-top:30px;
     background-image:url('../../public/img/background-pattern-grid-line.png');
    }
    /*sez.services-we-can */
    #services-we-can
    {background-image:url('../../public/img/background-pattern-grid-line.png');
     display: flex;
     margin-top: 30px;
    .card-side{
        width:50%;
        display:flex;
        flex-wrap:wrap;
        align-items: baseline;
      }
    }
}
</style>