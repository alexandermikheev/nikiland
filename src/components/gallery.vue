<script >
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

// import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
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
        <Carousel  :wrap-around="true">
        <Slide v-for="slide in 10" :key="slide">
            <div class="carousel__item"><img src="http://placehold.it/360x238" alt=""></div>
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