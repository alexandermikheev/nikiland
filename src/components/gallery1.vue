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
        modules: [Navigation, Pagination, Scrollbar, A11y, Virtual],
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
      <div id="gallery">
        <h2 class="gallery-header">Галерея</h2>
  <swiper
    v-if="small"
    :modules="modules"
    :slides-per-view="4"
    :space-between="50"
    navigation
    :rewind="true"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/1.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/2.png" alt=""></swiper-slide>
    <swiper-slide :v-slot="{ isActive }" class="swiper-gallery-slide"><img src="../assets/gallery/3.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/4.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/5.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/6.png" alt=""></swiper-slide>
  </swiper>


  <swiper
    v-else
    :modules="modules"
    :slides-per-view="1"
    :space-between="50"
    navigation
    :rewind="true"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/1.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/2.png" alt=""></swiper-slide>
    <swiper-slide :v-slot="{ isActive }" class="swiper-gallery-slide"><img src="../assets/gallery/3.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/4.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/5.png" alt=""></swiper-slide>
    <swiper-slide class="swiper-gallery-slide"><img src="../assets/gallery/6.png" alt=""></swiper-slide>
  </swiper>
</div>
</template>


<style >
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-gallery-slide{
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 360px;
  height: auto;
  border-radius: 40px;
  overflow: hidden;
}

.swiper-gallery-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>