<script >
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

// import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  data: () => ({
    width: 0,
    small: true,
    
}),
data() {
        return {
            slider:
            [
                {name: '1', link: '/src/assets/gallery/1.png'},
                {name: '2', link: '/src/assets/gallery/2.png'},
                {name: '3',link: '/src/assets/gallery/3.png'},
                {name: '3', link: '/src/assets/gallery/4.png'},
                {name: '4', link: '/src/assets/gallery/5.png'},
                {name: '5', link: '/src/assets/gallery/6.png'},
            ],      
        }
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

  },
  created() {
  window.addEventListener('resize', this.updateWidth);
  },
  name: 'WrapAround',
  components: {
    Carousel,
    Slide,
    Navigation,
  },
},

)
</script>

<template>
    <div id="gallery">
        <h2 class="gallery-header">Галерея</h2>
        <Carousel v-if="small" :items-to-show="3"  :wrap-around="true">
        <Slide v-for="slide in slider" :key="slide">
          <div class="promotions_carousel__item"> <slides class="carousel__item"><img src="/src/assets/gallery/1.png" alt=""></slides></div>
          <div class="promotions_carousel__item"><slides class="carousel__item"><img src="/src/assets/gallery/2.png" alt=""></slides></div>
          <div class="promotions_carousel__item"><slides class="carousel__item"><img src="/src/assets/gallery/3.png" alt=""></slides></div>
          <!-- <slides class="carousel__item"><img src="/src/assets/gallery/4.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/gallery/5.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/gallery/6.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/gallery/7.png" alt=""></slides> -->
        </Slide>
        <template #addons>
            <Navigation />
        </template>
        </Carousel>

        <Carousel v-else :items-to-show="1"  :wrap-around="true">
        <Slide v-for="(slide, index) in slider" :key="index">
          <div class="promotions_carousel__item"><slides class="carousel__item"><img src="/src/assets/gallery/1.png" alt=""></slides></div>
          <div class="promotions_carousel__item"><slides class="carousel__item"><img src="/src/assets/gallery/2.png" alt=""></slides></div>
          <div class="promotions_carousel__item"><slides class="carousel__item"><img src="/src/assets/gallery/3.png" alt=""></slides></div>
          <!-- <slides class="carousel__item"><img src="/src/assets/gallery/4.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/gallery/5.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/gallery/6.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/gallery/7.png" alt=""></slides> -->
        </Slide>
        <template #addons>
            <Navigation />
        </template>
        </Carousel>

    </div>
  </template>

<style scoped>
.carousel__item{
    border-radius: 40px;
    overflow: hidden;
}
.Carousel{
  padding: 10px;
}
#gallery{
    padding-bottom: 40px;
}
</style>