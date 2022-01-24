<template>
<div>
  <div class="autoplay">
    <h2>AutoPlay Example</h2>
  </div>
    <Carousel :autoplay="2000" :wrap-around="true">
    <Slide v-for="slide in hello" :key="slide.id">
      <div class="carousel__item"><img :src="slide.img" alt=""/></div>
    </Slide>

    <template #addons>
      <Pagination />
    </template>
  </Carousel>
</div>
</template>

<script>
import { Carousel, Pagination, Slide } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';
export default {
  name: 'Autoplay',
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
    Pagination,
  },
};
</script>
<style scoped>
.carousel__item {
  width:100%;
  height:50vh;
  margin:2% 0 2% 0;
}
.autoplay {
  text-align:center;
  margin-top:3%;
}
img {
  width:70%;
  height:50vh;
}
</style>