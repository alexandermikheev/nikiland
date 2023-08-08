<script>
  // import Swiper core and required modules
  import { Navigation, Pagination, Scrollbar, A11y, Virtual } from 'swiper/modules';

  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';
  import 'swiper/css/navigation';
  import 'swiper/css/pagination';
  import 'swiper/css/scrollbar';
  import 'swiper/css/virtual';

  // Import Swiper styles
  export default {
    data: () => ({
      width: 0,
      small: false,
    }),
    
    setup() {
    },

    destroyed() {
        window.removeEventListener("resize", this.updateWidth);
    },
    created() {
        window.addEventListener('resize', this.updateWidth);
    },
    beforeMount() {
        this.loadwidth()
    },
  methods : {
  updateWidth() {
    this.width = window.innerWidth;
    if(this.width < 1078){
      this.small = false
    }
    else{
      this.small = true;
     }
     
  },
  loadwidth(){
      if(window.innerWidth < 1078){
        this.small = false
      }
      else{
      this.small = true;
     }
     }
  },
  };
</script>

<template>
<div id="price">
    <h2 class="price-header">
        ПРАЙС
    </h2>
    <div class="price-card">
        <div class="price-card-list">
            <div class="weekdays">
                <h3 class="price-card-list-header">Прайс лист</h3>
                <h3 class="weekdays-header">в будние дни</h3>
                <div class="cost">30 мин - 400₽</div>
                <div class="cost">1 час - 600₽ </div>
            </div>
            <div class="weekends">
                <h3 class="weekends-header">в выходные дни</h3>
                <div class="cost">30 мин - 500₽</div>
                <div class="cost">1 час - 700₽</div>
            </div>
            <div class="cloud"></div>
            <div class="cloud1"></div>
            
        </div>
        <div class="price-card-aboniment">
            <h3 class="price-card-aboniment-header">Абонемент</h3>
            <div class="price-card-aboniment-quantity">
                <span>10</span>
                <h3 class="card-aboniment-header">Сеансов</h3>
                <p class="card-aboniment-header-paragraf">10 посещений по ( 1 часу ) - 5000₽</p>
            </div>
            <div class="smail-grut-blue"></div>
        </div>

    </div>
    <div class="price-footer">
        <div class="smail-grut-fil"></div>
        <div class="price-footer-header">
            <h2>территория радости и веселья</h2>
        </div>
        <div class="footer-back"></div>
    </div>
</div>

</template>

<style>
@keyframes cloudanimaton {
  0% {
    position: absolute;
    opacity: 1;
  }
  50% {
    opacity: 0;

  }
  100% {
    opacity: 1;
  }
}
.price-card{
    display: flex;
    justify-content: space-evenly;
    margin-bottom: 337px;
    height: 400px;
}

.price-card-list{
    background-image: url(../assets/oblako.svg);
    background-position: center center;
    background-repeat: no-repeat;
    width: 425px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: #FFFFFF;
    font-family: Montserrat;
    font-size: 24px;
    font-weight: bold;
    position: relative;

}
.price-card-aboniment-quantity span{
    border-radius: 100%;
    padding: 30px 30px;
    background-color: #8AC8E5;
    display: block;
}
.weekdays-header {
   display: flex;
   flex-direction: column;
}
.price-card-aboniment{
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    justify-content: flex-end;
}
.price-card-aboniment-header, .card-aboniment-header{
    font-family: 'PoetsenOne';
    color: #676091;
    font-size: 38px;

}
.price-card-aboniment-header{
    margin-top: 32px;
    margin-bottom: 32px;
}
.card-aboniment-header{
    margin-top: 17px;
    margin-bottom: 13px;
}
.card-aboniment-header-paragraf{
    font-family: 'Montserrat-ex-bold';
    font-size: 16px;
    color: #8AC8E5;
    font-weight: bold;
    margin: 0;
}
.price-card-aboniment-quantity{
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #676091;
}

.price-card-aboniment-quantity span{
    font-family: 'PoetsenOne';
    font-size: 84px;
}


.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg);
    width: 299px;
    height: 338px;
    top: -198%;
    left: 2%;
}
.smail-grut-blue{
    position: absolute;
    background: url(../assets/smail-grut-blue.svg);
    width: 340px;
    height: 338px;
    top: 400px;
    left: -310px;
}
.cloud{
    position: absolute;
    background: url(../assets/cloud.svg);
    width: 27.975px;
    height: 21.415px;
    top: 530px; 
    left: 110px;
    animation: cloudanimaton 1s linear infinite;
}
.cloud1{
    position: absolute;
    background: url(../assets/cloud.svg);
    background-repeat: no-repeat;
    background-size: contain;
    width: 60px;
    height: 45px;
    top: 450px; 
    left: 160px;
    animation: cloudanimaton 1s linear infinite;
}
.price-card-list-header{
    margin: 0;
    font-size: 26px;
    text-align: center;
    text-transform: uppercase;
    line-height: 38.6px;
}
.weekdays-header, .weekends-header{
    margin: 0;
    color: #676091;
    font-size: 16px;
    line-height: 35.6px;
}
.cost{
    font-size: 28px;
    font-weight: bolder;
    font-family: "Montserrat-bold";
    font-weight: bold;
    line-height: 30px;
}
.cost:nth-child(n+2){
    margin-bottom: 5px;
}
.price-footer{
    height: 170px;
    display: flex;
    background-color: #676091;
    align-items: center;
    justify-content: first baseline;
    position: relative;
}
.price-footer-header{
    color: #FFFFFF;
    font-family: 'PoetsenOne-bold';
    font-size: 32px;
    margin-left: 10%;
}
.footer-back{
    position: absolute;
    background: url(/src/assets/price-footer/smail-blue.svg) bottom left no-repeat, url(/src/assets/price-footer/smail-fil.svg) 72% 19% no-repeat, url(/src/assets/price-footer/smail-j.svg) 93% bottom no-repeat;    height: 200px;
    width: 100%;
    top: -18%;
}
@media (min-width: 1201px) {}

@media (min-width: 641px) and (max-width: 1200px) {
    .price-card{
    display: flex;
    flex-direction: column-reverse;
    margin: 0 0;
    margin-bottom: 67%;
}
.price-card-list{
    padding: 75px 0;
    width: 100%;
    margin-bottom: 366px;
    margin-bottom: 170%;
    margin-top: 5%;
}
.price-card-aboniment {
    align-items: flex-start;
    margin-top: 119%;
    background: url(../assets/price-footer/yellow-smail-price.svg) 144% 54%/81% no-repeat;
}
.price-card-aboniment-header {
    margin-left: 26px;
}
.price-card-aboniment-quantity{
    margin-left: 10px;
}
.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg);
    width: 299px;
    height: 338px;

    top: -157%;
    left: 39px;
}
.smail-grut-blue{
    position: absolute;
    display: none;
    width: 340px;
    height: 338px;
    top: 0%;
    left: 20%;

}
.cloud{
    top: 530px;
    left: 286px;
}
.cloud1{
    top: 433px;
    left: 300px;
}
@media (min-width: 1001px) and (max-width: 1200px){
    .price-card-aboniment {
    align-items: flex-start;
    margin-top: 119%;
    background: url(../assets/price-footer/yellow-smail-price.svg)  85% 55%/30% no-repeat;
}
.price-card-aboniment-quantity span {
    font-size: 90px;
    background-color: #F7C400;
}
.price-card-aboniment-header, .card-aboniment-header {
    font-family: 'PoetsenOne';
    color: #676091;
    font-size: 36px;
}
.price-card-aboniment-header {
    margin-left: 77px;
}
.card-aboniment-header-paragraf {
    font-size: 18px;
}
.price-card-list{
    background-size: 37%;
    margin-bottom: 71%;
}
.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg) no-repeat;
    background-size: 68%;
    top: -239%;
}
.cloud {
    top: 555px;
    left: 190px;
}
.cloud1 {
    top: 443px;
    left: 285px;
}
.price-footer-header {
    font-size: 16px;
    margin: auto;
}
.price-footer {
    height: 96px;
}
.footer-back{
    background: url(/src/assets/price-footer/smail-blue.svg) -5% 69% no-repeat, url(/src/assets/price-footer/smail-j.svg) 98% -6% no-repeat;
}

}
}
@media (max-width: 640px) {
.price-card{
    display: flex;
    flex-direction: column-reverse;
    margin: 64% 0px;
}
.price-card-list{
    padding: 75px 0;
    width: 100%;
    margin-bottom: 366px;
    margin-bottom: 170%;
    margin-top: 5%;
}
.price-card-aboniment {
    align-items: flex-start;
    margin-top: 119%;
    background: url(../assets/price-footer/yellow-smail-price.svg) 144% 54%/81% no-repeat;
}
.price-card-aboniment-header {
    margin-left: 43px;
}
.price-card-aboniment-quantity{
    margin-left: 10px;
}
.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg);
    width: 299px;
    height: 338px;
    top: -198%;
    left: 39px;
}
.smail-grut-blue{
    position: absolute;
    display: none;
    width: 340px;
    height: 338px;
    top: 0%;
    left: 20%;

}
.cloud{
    top: 530px;
    left: 286px;
}
.cloud1{
    top: 433px;
    left: 300px;
}
.footer-back{
    position: absolute;
    background: url(/src/assets/price-footer/smail-blue.svg) -4% 96% no-repeat, url(/src/assets/price-footer/smail-j.svg) 93% -3% no-repeat;
    height: 200px;
    width: 100%;
    top: -18%;
}
.price-footer-header{
        margin-left: 0;
        text-align: center;
}
.price-card-aboniment-quantity span{
    background-color: #F7C400;
}
}
@media (min-width: 801px) and (max-width: 1000px){
    .price-card-aboniment {
    align-items: flex-start;
    margin-top: 119%;
    background: url(../assets/price-footer/yellow-smail-price.svg)  90% 54%/41% no-repeat;
}
.price-card-aboniment-quantity{
    margin-left: 50px;
}
.price-card-aboniment-quantity span {
    font-size: 90px;
    background-color: #F7C400;
}
.price-card-aboniment-header, .card-aboniment-header {
    font-family: 'PoetsenOne';
    color: #676091;
    font-size: 36px;
}
.price-card-aboniment-header {
    margin-left: 108px;
}
.card-aboniment-header-paragraf {
    font-size: 18px;
}
.price-card-list{
    background-size: 45%;
    margin-bottom: 71%;
}
.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg) no-repeat;
    background-size: 45%;
    top: -157%;
}
.cloud {
    top: 534px;
    left: 143px;
}
.cloud1 {
    top:  421px;
    left: 184px;
}
.price-footer-header {
    font-size: 16px;
    margin: auto;
}
.price-footer {
    height: 96px;
}
.footer-back{
    background: url(/src/assets/price-footer/smail-blue.svg) -5% 69% no-repeat, url(/src/assets/price-footer/smail-j.svg) 98% -6% no-repeat;
}

}
@media (min-width: 641px) and (max-width: 800px){
    .price-card-aboniment {
    align-items: flex-start;
    margin-top: 119%;
    background: url(../assets/price-footer/yellow-smail-price.svg) 106% 54%/48% no-repeat;
}
.price-card-aboniment-quantity span {
    font-size: 90px;
    background-color: #F7C400;
}
.price-card-aboniment-header, .card-aboniment-header {
    font-family: 'PoetsenOne';
    color: #676091;
    font-size: 36px;
}
.price-card-aboniment-header {
    margin-left: 70px;
}
.card-aboniment-header-paragraf {
    font-size: 18px;
}
.price-card-list{
    background-size: 50%;
    margin-bottom: 89%;
}
.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg) no-repeat;
    background-size: 45%;
    top: -157%;
}
.cloud {
    top: 534px;
    left: 143px;
}
.cloud1 {
    top:  421px;
    left: 184px;
}
.price-footer-header {
    font-size: 16px;
    margin: auto;
}
.price-footer {
    height: 96px;
}
.footer-back{
    background: url(/src/assets/price-footer/smail-blue.svg) -5% 69% no-repeat, url(/src/assets/price-footer/smail-j.svg) 98% -6% no-repeat;
}

}


@media (min-width: 482px) and (max-width: 605px){

    .smail-grut-fil {
    position: absolute;
    background: url(/src/assets/smail-grut-fil.svg) no-repeat;
    background-size: 68%;
    width: 299px;
    height: 342px;
    top: -134%;
    left: 39px;
}

}

@media (min-width: 426px) and (max-width: 482px){

.smail-grut-fil {
    position: absolute;
    background: url(/src/assets/smail-grut-fil.svg) no-repeat;
    background-size: 40%;
    width: 299px;
    height: 342px;
    top: -79%;
    left: 39px;
}

}
@media (min-width: 426px) and (max-width: 640px){

    .price-card-aboniment {
        background: url(../assets/price-footer/yellow-smail-price.svg) 116% 54%/63% no-repeat;
    }


}


@media (min-width: 376px) and (max-width: 425px){
    .price-card-aboniment {
    align-items: flex-start;
    margin-top: 119%;
    background: url(../assets/price-footer/yellow-smail-price.svg) 106% 54%/48% no-repeat;
}
.price-card-aboniment-quantity span {
    font-size: 37px;
}
.price-card-aboniment-header, .card-aboniment-header {
    font-family: 'PoetsenOne';
    color: #676091;
    font-size: 24px;
}
.price-card-aboniment-header {
    margin-left: 61px;
}
.card-aboniment-header-paragraf {
    font-size: 14px;
}
.price-card-list{
    background-size: 92%;
}
.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg) no-repeat;
    background-size: 45%;
    top: -157%;
}
.cloud {
    top: 534px;
    left: 143px;
}
.cloud1 {
    top:  421px;
    left: 184px;
}
.price-footer-header {
    font-size: 16px;
    margin: auto;
}
.price-footer {
    height: 96px;
}
.footer-back{
    background: url(/src/assets/price-footer/smail-blue.svg) -5% 69% no-repeat, url(/src/assets/price-footer/smail-j.svg) 98% -6% no-repeat;
}

}

@media (min-width: 320px) and (max-width: 375px){
    
.price-card-aboniment {
    align-items: flex-start;
    margin-top: 119%;
    background: url(../assets/price-footer/yellow-smail-price.svg) 106% 54%/48% no-repeat;
    
}
.price-card-aboniment-quantity span {
    font-size: 37px;
}
.price-card-aboniment-header, .card-aboniment-header {
    font-family: 'PoetsenOne';
    color: #676091;
    font-size: 24px;
}
.price-card-aboniment-header {
    margin-left: 61px;
}
.card-aboniment-header-paragraf {
    font-size: 14px;
}
.price-card-list{
    background-size: 92%;
}
.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg) no-repeat;
    background-size: 45%;
    top: -155%;
}
.cloud {
    top: 482px;
    left: 143px;
}
.cloud1 {
    top: 379px;
    left: 184px;
}
.price-footer-header {
    font-size: 16px;
}
.price-footer {
    height: 96px;
}
.footer-back{
    background: url(/src/assets/price-footer/smail-blue.svg) -5% 57% no-repeat, url(/src/assets/price-footer/smail-j.svg) 98% 48% no-repeat;
}

}

</style>