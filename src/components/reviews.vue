<script>
  import { Navigation, Pagination, Scrollbar, A11y, Virtual, Autoplay } from 'swiper/modules';
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import 'swiper/css';
  import 'swiper/css/navigation';
  import 'swiper/css/pagination';
  import 'swiper/css/scrollbar';
  import 'swiper/css/virtual';

  export default {
    data: () => ({
      width: 0,
      small: true,
    }),
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Navigation, Pagination, Scrollbar, A11y, Autoplay],
      };
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
  
  created() {
  window.addEventListener('resize', this.updateWidth);
  },
  beforeMount() {
    this.loadwidth()
},
  };
</script>

<template>
<div id="reviews" >
    <div class="reviews-header">Что говорят о нас</div>
    <div class="reviews-paragraf">Из наших книг отзывов и предложений</div>
    
    <div class="reviews-card" v-if="small">
        <div class="reviews-card-item feedback-1">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Саларис"</div>
        </div>
        <!-- <div class="reviews-card-item feedback-2">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
        <div class="reviews-card-item feedback-3">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
        <div class="reviews-card-item feedback-4">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
        <div class="reviews-card-item feedback-5">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
        <div class="reviews-card-item feedback-6">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div> -->
    </div>

    <swiper
    v-else
    :modules="modules"
    :slides-per-view="1"
    :space-between="10"
    navigation
    :loop="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide class="swiper-reviews-slide">
        <div class="reviews-card-item feedback-6">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Саларис"</div>
        </div>
    </swiper-slide>
    <!-- <swiper-slide class="swiper-reviews-slide">
        <div class="reviews-card-item feedback-2">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
    </swiper-slide>
    <swiper-slide class="swiper-reviews-slide">
        <div class="reviews-card-item feedback-3">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
    </swiper-slide>
    <swiper-slide class="swiper-reviews-slide">
        <div class="reviews-card-item feedback-4">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
    </swiper-slide>
    <swiper-slide class="swiper-reviews-slide">
        <div class="reviews-card-item feedback-5">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div>
    </swiper-slide>
    <swiper-slide class="swiper-reviews-slide">
        <div class="reviews-card-item feedback-6">
            <div class="reviews-card-paragraf">Отлично отдохнули и отпраздновали день рождения дочери. Отличное место для детей и взрослых. Дети лазили в лабиринте их было видно, но не слышно!</div>
            <div class="reviews-card-place">ТЦ "Авиапарк"</div>
        </div> -->
    <!-- </swiper-slide> -->

  </swiper>
    
</div>




 <div id="about">
    <div class="about-header">
        ЕСЛИ ВЫ ХОТИТЕ ОТКРЫТЬ НАШ ЦЕНТР В СВОЁМ ТЦ ОБРАТИТЕСЬ ПО EMAIL:
    </div>
    <div class="phone-info">
        <div class="phone-about">
            <a href="mailto:info@nikiland.club">info@nikiland.club</a>
        </div>
    </div>

</div> 
</template>

<style >
#reviews{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.reviews-card{
    display: inline-flex;
    align-items: flex-start;
    gap: 40px;
    justify-content: center;
    flex-wrap: wrap;
    width: 80%;
    }
.reviews-card-item{
    padding: 20px;
    background: #F7C400;
    color: #ffffff;
    font-family: "Montserrat";
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
}
.reviews-card-paragraf{
    width: 320px;
}
.phone-about{
    border-radius: 20px;
    background: #2FAC4A;
    width: 321px;
    height: 59px;
    display: flex;
    justify-content: center;
    align-items: center;

}
.phone-about a{
    color: #FFF;
    overflow: hidden;
    text-overflow: ellipsis;
    font-family: Montserrat;
    font-size: 24px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    text-transform: lowercase;
    text-decoration: none;
}
.phone-info{
    display: flex;
    justify-content: center;
    padding-bottom: 40px;
}
.about-header{
    width: 50%;
    margin: auto;
}
.reviews-paragraf{
    color: #9D9D9D;
    text-align: center;
    font-family: Montserrat;
    font-size: 17px;
    font-style: normal;
    font-weight: 500;
    line-height: 140%;
    text-transform: lowercase;
    padding-bottom: 40px;
}
.reviews-header{
    padding-bottom: 0;
}
.feedback-1{
    background-color: #DF5F26;
}
/* .feedback-2{
    background-color: #DF5F26;
} */
.feedback-3{
    background-color: #695C91;
}
.feedback-5{
    background-color: #8AC8E5;
}
.feedback-6{
    background-color: #DF5F26;
}
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-reviews-slide{
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 360px;
  height: auto;
  /* overflow: hidden; */
  /* margin-right: 30px; */
}

.swiper-reviews-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
@media (max-width: 640px) {

    .about-header{
        width: 90%;
    }
    
}
</style>