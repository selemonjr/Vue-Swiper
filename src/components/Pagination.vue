<template>
<div class="example-2">
    <div class="pagination">
    <h2>Pagination Example</h2>
</div>
  <Carousel :settings='settings' :breakpoints='breakpoints'>
    <Slide v-for='slide in hello' :key='slide.id'>
      <div class='carousel_item'><img :src="slide.img" alt="" /></div>
    </Slide>

    <template #addons>
      <Pagination />
      <Navigation />
    </template>
  </Carousel>
</div>
</template>

<script>
import { Carousel, Navigation, Slide, Pagination } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';
export default {
  name: 'ExamplePagination',
  components: {
    Pagination,
    Carousel,
    Slide,
    Navigation,
  },
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
        },
        {
            id:4,
            img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse4.mm.bing.net%2Fth%3Fid%3DOIP.ON-2ncPOAZEXu6EeniTIDAHaD4%26pid%3DApi&f=1"
        },
        {
            id:5,
            img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.a8VSqSl--UmzsOBdWn2EtgHaE8%26pid%3DApi&f=1"
        },
        {
            id:6,
            img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.rIWz1RRvrR1g8uJrHFUzewHaD4%26pid%3DApi&f=1"
        },
        {
            id:7,
            img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP._b5z0ASYBeE8Q6B7conVBwHaE8%26pid%3DApi&f=1"
        },
        {
            id:8,
            img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.EC8rYaXyxu_9dDSuH5wRkwHaE8%26pid%3DApi&f=1"
        },
        {
            id:9,
            img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.I77NluT5d8yAAnL8v_0NQgHaFj%26pid%3DApi&f=1"
        },
          {
            id:10,
            img:"https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.jgqXzaWcMsYA5jivh1L-gQHaFh%26pid%3DApi&f=1"
        }
      ]
    }
  },
     // carousel settings
    settings: {
      itemsToShow: 1,
      snapAlign: 'center',
    },
    // breakpoints are mobile first
    // any settings not specified will fallback to the carousel settings
    breakpoints: {
      // 700px and up
      700: {
        itemsToShow: 3.5,
        snapAlign: 'center',
      },
      // 1024 and up
      1024: {
        itemsToShow: 5,
        snapAlign: 'start',
      },
    },
  }
</script>
<style scoped>
.example-2 {
    margin-top:2%;
    width:95%;
    margin-left:2%;
    text-align:center;
}
.pagination {
    text-align:center;
    margin:1% 0 1% 0;
}
img {
    width:100%;
    height:300px;
}
</style>