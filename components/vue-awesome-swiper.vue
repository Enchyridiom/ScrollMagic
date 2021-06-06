
<template>
<swiper :pagination="{
  'type': 'fraction'
}" :navigation="true" class="mySwiper">
  <swiper-slide>Slide 1</swiper-slide><swiper-slide>Slide 2</swiper-slide><swiper-slide>Slide 3</swiper-slide><swiper-slide>Slide 4</swiper-slide><swiper-slide>Slide 5</swiper-slide><swiper-slide>Slide 6</swiper-slide><swiper-slide>Slide 7</swiper-slide><swiper-slide>Slide 8</swiper-slide><swiper-slide>Slide 9</swiper-slide>
  </swiper>
</template>



<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from '../plugins/vue-awesome-swiper';

// Import Swiper styles
import '../assets/css/swiper.css';

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
  methods: {
    
  }
  
}
</script>

<style>
</style>