<script >
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
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
        <Carousel :items-to-show="3" :wrap-around="true">
        <Slide v-for="slide in 3" :key="slide">
            <div class="promotions_carousel__item"><img src="http://placehold.it/360x476" alt=""></div>
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