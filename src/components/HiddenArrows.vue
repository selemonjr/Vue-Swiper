<template>
<div class="example-3">
    <div class="arrows">Hidden Arrows</div>
      <Carousel>
    <Slide v-for="slide in hello" :key="slide.id">
      <div class="carousel__item"><img :src="slide.img" alt=""/></div>
    </Slide>

    <template #addons>
      <Navigation />
    </template>
  </Carousel>
</div>
</template>

<script>
import { Carousel, Navigation, Slide } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';

export default{
  name: 'Breakpoints',
    data() {
    return {
      hello : [
        {
          id:1,
          img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse4.mm.bing.net%2Fth%3Fid%3DOIP.ytLp532ymT0rspTOvO2MzAHaD4%26pid%3DApi&f=1"
        },
        {
          id:2,
          img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.9pkusdV8Qqj2yLDMSJkcRQHaEK%26pid%3DApi&f=1"
        },
        {
          id:3,
          img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.bzrShSWMuxd96oCAKAc0ZgHaDt%26pid%3DApi&f=1"
        }
      ]
    }
  },
  components: {
    Carousel,
    Slide,
    Navigation,
  },
};
</script>

<style scoped>
.arrows {
    text-align:center;
    margin-top:3%;
    margin-bottom:3%;
}
.example-3 {
    width:90%;
    height:50vh;
    text-align:center;
    margin-left:5%;
}
img {
    width:100%;
    height:200px;
}
.carousel__prev--in-active,
.carousel__next--in-active {
  display: none;
}
</style>