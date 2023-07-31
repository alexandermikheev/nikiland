<script >
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  data: () => ({
    width: 0,
    small: true,
    
}),

methods : {
  updateWidth() {
    this.width = window.innerWidth;
    if(this.width < 1078){
      this.small = false;
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
})
</script>

<template>
    <div id="promotions">
        <h2 class="promotions-header">акции и события</h2>
        <Carousel v-if="small" :items-to-show="3" :wrap-around="true">
        <Slide v-for="slide in 1" :key="slide">
            <slides class="carousel__item"><img src="/src/assets/promo/1.png" alt=""></slides>
            <slides class="carousel__item"><img src="/src/assets/promo/2.png" alt=""></slides>
            <slides class="carousel__item"><img src="/src/assets/promo/3.png" alt=""></slides>
        </Slide>
    
        <template #addons>
            <Navigation />
        </template>
        </Carousel>

        <Carousel v-else :items-to-show="1" :wrap-around="true">
        <Slide v-for="slide in 1" :key="slide">
          <slides class="carousel__item"><img src="/src/assets/promo/1.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/promo/2.png" alt=""></slides>
          <slides class="carousel__item"><img src="/src/assets/promo/3.png" alt=""></slides>
        </Slide>
    
        <template #addons>
            <Navigation />
        </template>
        </Carousel>
    </div>
  </template>

<style scoped>

#promotions{
    padding-bottom: 40px;
}
</style>