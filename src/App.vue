<template>
  <div>
    <Navigation/>
    <Pagination/>
    <Swiper/>
    <HiddenArrows/>
  </div>
</template>

<script>
import Swiper from './components/Swiper.vue';
import Navigation from "./components/Navigation.vue";
import Pagination from "./components/Pagination.vue";
import HiddenArrows from "./components/HiddenArrows.vue";
export default {
  name: 'App',
  components: {
    Navigation,
    Swiper,
    Pagination,
    HiddenArrows,
  }
}
</script>

<style>
* {
  margin:0;
  padding:0;
  box-sizing:border-box;
}
body {
  position:relative;
  width:100%;
  height:100vh;
  font-family:sans-serif;
}
</style>
