<template>
  <div>
    <swiper :options="swiperOption" class="swiper">
      <swiper-slide data-aos="fade-in" data-aos-duration="1000" class="silde" style="background-image:url(image/top1.jpg);">
        <v-layout data-aos="fade-up" data-aos-duration="1000" fill-height align-center justify-center>
          <div class="slog">명지전문대학 배지원</div>
        </v-layout>
      </swiper-slide>
      
      <swiper-slide class="silde" style="background-image:url(image/top2.jpg);">
        <v-layout fill-height align-center justify-center>
          <div class="slog">열심히 하겠습니다</div>
        </v-layout>
      </swiper-slide>
     
      <swiper-slide class="silde" style="background-image:url(image/top3.jpg);">
        <v-layout fill-height align-center justify-center>
          <div class="slog">뽑아주세요</div>
        </v-layout>
      </swiper-slide>
      </swiper>
    

      <div class="section">
      <div class="header">프로젝트 목록</div>
      <v-layout wrap>
       
        <v-flex xs4 class="pa-2" data-aos="fade-right">
          <v-responsive :aspect-ratio="1/1">
            <img src="image/top1.jpg" class="image">
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2" data-aos="fade-down" data-aos-delay="100">
          <v-responsive :aspect-ratio="1/1">
            <img src="image/top2.jpg" class="image">
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2" data-aos="fade-left" data-aos-delay="200">
          <v-responsive :aspect-ratio="1/1">
            <img src="image/top3.jpg" class="image">
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2" data-aos="fade-right">
          <v-responsive :aspect-ratio="1/1">
            <img src="image/top2.jpg" class="image">
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2">
          <v-responsive :aspect-ratio="1/1" data-aos="fade-up"  data-aos-delay="100">
            <img src="image/top3.jpg" class="image">
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2">
          <v-responsive :aspect-ratio="1/1" data-aos="fade-left" data-aos-delay="200">
            <img src="image/top1.jpg" class="image">
          </v-responsive>
        </v-flex>
        
      
      </v-layout>
    </div>

  </div>
</template>

<script>
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
  import 'swiper/swiper-bundle.css'
  import AOS from "aos"
  import "aos/dist/aos.css";
  export default {
    name: 'Home',
    data(){
      return {
        swiperOption:{
          loop:true,
          autoplay:{
            delay:1000
          }
        }
      }
    },
    mounted(){
      AOS.init()
    },
    components:{
      Swiper,
      SwiperSlide
    }

   
  }
</script>
<style scoped lang="less">
  .swiper{
    height:100vh;
    .slide{
      background-size:cover;
      background-position: center center;
      .slog{
        font-size:60px;
        font-weight:bold;
        color:white;
      }
    }
  }

  .section{
    width:1190px;
    margin: 0 auto;
    padding-top:40px;
    padding-bottom:40px;
    .header{
      text-align:center;
      font-size:40px;
      font-weight:bold;
    }
    .image{
      width:100%;
      height:100%;
      object-fit: cover;
    }
  }

</style>
