<script setup>
import card2 from "@/components/cards/card2.vue";
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation} from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';
import datafiles2 from '@/views/DataFiles2.js'
const breakpoints={
      '400': {
        slidesPerView: 1,
        spaceBetween: 0,  
      },  
      '768': {
        slidesPerView: 2,
        spaceBetween: 10,
      },

      '1240': {
        slidesPerView: 3,
        spaceBetween: 5,
      },
      '1440': {
        slidesPerView: 3,
        spaceBetween: 10,
      },
    }
const modules = [Navigation]




</script>


<template>
    <section class="section-2">
      
      <h3 class="section-2-title">{{ $t('Visa Support') }}</h3>
         <p  class="section-2-info">{{ $t('Experience stress-free travel with our expert visa support. We provide seamless assistance and comprehensive guidance, ensuring a smooth journey') }}</p>

  <swiper class="corusel-1" 
:slides-per-view="1"
:space-between="80"
:breakpoints="breakpoints"
:navigation="true" 
:modules="modules"

>

<swiper-slide v-for="item in datafiles2" :key="item">
  <card2 :info2="item"/>
</swiper-slide>


</swiper>

    </section>
</template>



<style>

</style>