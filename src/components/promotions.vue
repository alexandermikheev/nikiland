<script>
  // import Swiper core and required modules
  import { Navigation, Pagination, Scrollbar, A11y, Virtual, Autoplay } from 'swiper/modules';

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

  destroyed() {
  window.removeEventListener("resize", this.updateWidth);
  },
  created() {
  window.addEventListener('resize', this.updateWidth);
  },  beforeMount() {
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
    <div id="promotions">
        <h2 class="promotions-header">акции и события</h2>

    <div v-if="small" class="promo">
      <div class="promo-box"><img src="../assets/promo/1.png" alt=""></div>
    <div class="promo-box midle"><img src="../assets/promo/2.png" alt=""></div>
    <div class="promo-box"><img src="../assets/promo/3.png" alt=""></div>
    </div>

  <swiper
    v-else
    :modules="modules"
    :slides-per-view="1"
    :loop="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    navigation
  >
    <swiper-slide class="swiper-slide-promotions mb"><img src="../assets/promo/1.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-slide-promotions mb"><img src="../assets/promo/2.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-slide-promotions mb"><img src="../assets/promo/3.png" alt=""></swiper-slide>
  </swiper>
</div>

</template>
<style >

.promo{
  display: flex;
  justify-content: center;
}
.midle{
  margin: 0 40px;
}

.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide-promotions{
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 20px;
  width: 360px;
  height: auto;
}

.swiper-slide-promotions img {
  display: block;
  object-fit: cover;
}
@media (min-width: 1201px) {}

@media (min-width: 641px) and (max-width: 1200px) {
  .swiper-slide-promotions{
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 0;
  width: 360px;
  height: auto;
}
}

@media (max-width: 640px) {
  .swiper-slide-promotions{
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 0;
  width: 360px;
  height: auto;
}

}


@media (min-width: 376px) and (max-width: 425px){
  .swiper-slide-promotions{
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 0;
  width: 360px;
  height: auto;
}

}
@media (min-width: 320px) and (max-width: 375px){
  .swiper-slide-promotions{
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 0;
  width: 360px;
  height: auto;
}
}


</style>