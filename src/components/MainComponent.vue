<template>
<div>
    <!--sez. let-passion-->
    <div id="let-passion">
        <div class="testo">
             <p>Let passion and determination be the guide along the way and develop at your own pace that's comfortable</p>
             <span>FANNIE MORENO</span>
             <span>Founder &#38; CEO</span>
        </div>
        <div class="info-in-numeri">
            <div class="info">
                <span class="green">1.926</span>
                <span>FINISHED SESSIONS</span>
            </div>
             <div class="info">
                <span class="green">3.092+</span>
                <span>ENROLLED LEARNERS</span>
            </div>
            <div class="info">
                <span class="green">200</span>
                <span>ONLINE INSTRUCTORS</span>
            </div>
             <div class="info">
                <span class="green">100%</span>
                <span>SATISFACTION RATE</span>
             </div>
        </div>
    </div>

    <!--sez. services-we-can-->
    <div id="services-we-can">
        <div class="card-side" >
            <!--CardImgDown :titolo="titoloGraphicDesign" :testo="testoGraphicDesign" :urlImg="urlImgGraphicDesign"/-->
            <div class="img-down">
                <CardImgDown :informationObject="cardImgDownInformation"/>
                <div class="graphic-design">
                    <h2>Graphic Design</h2>
                    <p>Have a passion for graphics and art? Show your talents with confidence and self assertiveness </p>
                    <img src="../../public/img/home-6-service-image-01.png" alt="">
                </div>
                <div class="business-administration">
                    <h2>Business Administration</h2>
                    <p>Learners are encouraged to study the mechanism and structure of system administration</p>
                    <img src="../../public/img/home-6-service-image-02.png" alt="">
                </div>
            </div>
            <div class="img-up">
                <div class="idea-discussion">
                     <img src="../../public/img/home-6-service-image-03.png" alt="">
                     <h2>Idea Discussion</h2>
                     <p>Get teamed up with the specialist who work and teach coding for years at famous university </p>
                </div>
                <div class="web-development">
                    <img src="../../public/img/home-6-service-image-04.png" alt="">
                    <h2>Web Development</h2>
                    <p>Get teamed up with the specialist who work and teach coding for years at famous university </p>
                </div>
            </div>
        </div>
        <div class="elenco">
            <h3>TOGETHER WE CAN CREATE </h3>
            <h1>SERVICES WE CAN PROVIDE FOR MY CLIENTS</h1>
            <ul>
                <li><i class="fa-solid fa-check"></i>Select and customize courses to your preferences</li>
                <li><i class="fa-solid fa-check"></i>Change the tutor and make arrangements</li>
                <li><i class="fa-solid fa-check"></i>Partecipate in events to join others</li>
                <li><i class="fa-solid fa-check"></i>Get the desired certificate delivered at house</li>
            </ul>
            <div class="button">
                <ButtonComponent :messageButton="message"/>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
import CardImgDown from './CardImgDown.vue'
export default {
name:'MainComponent',

data(){
    return{
        cardImgDownInformation:[    //array di oggetti
            {
                titolo:'Graphic Design',
                testo:'Have a passion for graphics and art? Show your talents with confidence and self assertiveness',
                imgUrl:'../../public/img/home-6-service-image-01.png'
            }
        ],
        /*
        titoloGraphicDesign:'Graphic Design',
        testoGraphicDesign:'Have a passion for graphics and art? Show your talents with confidence and self assertiveness',
        urlImgGraphicDesign:'../../public/img/home-6-service-image-01.png',
        testoBusinessAdministration:'Learners are encouraged to study the mechanism and structure of system administration'*/
        message:'Get started for free'
    }
},

 components:{
     ButtonComponent,
     CardImgDown
 }
}
</script>

<style lang="scss" scoped>
/*sez.let-passion*/
#let-passion{
    display:flex;
    flex-direction:column;
    align-items: center;
    margin-top:30px;
    background-image:url('../../public/img/background-pattern-grid-line.png');
    .testo{
        width:40%;
        display:flex;
        flex-direction:column;
        align-items: center;
         p{
             font-size:30px;
         }
    }
    .info-in-numeri{
        display: flex;
        .info{
             display: flex;
             flex-direction: column;
             justify-content: center;
             padding:20px;
             .green{
                color:#1fad96;
                text-align: center;
                  }

             }
    }
    .elenco{
        display: flex;
        flex-direction:column;
    }
}
/*sez.services-we-can */
#services-we-can{
    background-image:url('../../public/img/background-pattern-grid-line.png');
    display: flex;
    .card-side{
        width:50%;
        margin-top:30px;
        .img-down{
            display:flex;
            .graphic-design, .business-administration{
                display:flex;
                flex-direction:column;
                background-color: #ffffff;
                padding:20px;
                img{
                    width:150px;
                    flex-grow:1;
                    }
                }
         }
        .img-up{
            display:flex;
            .idea-discussion,.web-development{
                display:flex;
                flex-direction:column;
                width:50%;
                padding:20px;
                img{
                     width:150px;
                    flex-grow:1;
                    }
             }
        }
    }
    .elenco{
        width:50%;
        display:flex;
        flex-direction: column;
        justify-content: space-evenly;
        ul{
            list-style-type:none;
            li{
                margin-bottom: 20px;
            }
            li i{
                margin-right:20px;
                color:#1fad96;
            }
        }
        .button{
            width:50%;
        }
    }
}
</style>