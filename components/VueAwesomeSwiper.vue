
<template>
  <swiper :pagination="{
    'type': 'fraction'
    }" :navigation="true" class="mySwiper">
    <swiper-slide>Slide 1</swiper-slide><swiper-slide>Slide 2</swiper-slide><swiper-slide>Slide 3</swiper-slide><swiper-slide>Slide 4</swiper-slide>
    

    <!-- <img :src="'/bocal6.png'" alt="demo"> -->


  </swiper>
</template>



<script>
import { Swiper, SwiperSlide } from '../plugins/vue-awesome-swiper';

// Import Swiper styles
/* import 'swiper/swiper.scss'; */

import "swiper/components/pagination/pagination.min.css"
import "swiper/components/navigation/navigation.min.css"

import '../assets/css/swiper.css';

// import Swiper core and required modules

import SwiperCore, {
  Pagination,Navigation
} from 'swiper/core';

// install Swiper modules
SwiperCore.use([Pagination,Navigation]);

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
        
        
    };
  },
/*   methods: {
    
  } */
  
}
</script>

<style>

/* #app { height: 100% } */
html,
body {
  position: relative;
  height: 100%;
}

body {
  background: white;
  font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
  font-size: 14px;
  color: #000;
  margin: 0;
  padding: 0;
}

.swiper-container {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>