<template>
  <div class="slidearea ps-0">
    <div class="silder-three">
      <Swiper
        class="swiper-container main-silder-swiper-03"
        :modules="module"
        :speed="1500"
        :loop="true"
        :parallax="true"
        :pagination="pagination"
        :navigation="{
          prevEl: '.btn-prev',
          nextEl: '.btn-next'
        }"
        :autoplay="{ delay: 1500 }"
      >
        <SwiperSlide class="swiper-slide" v-for="({ img }, ind) in mainSlider" :key="ind">
          <div class="silder-content" data-swiper-parallax="-40%">
            <div class="container">
              <div class="inner-content row align-items-center g-0">
                <div class="col-md-6">
                  <div class="inner-text">
                    <h6 class="text text-primary">What We Do</h6>
                    <h3 class="title">
                      Architeture With<br />
                      A<span class="text-primary">Different</span> Approach
                    </h3>
                    <p>
                      If you are going to use a passage of Ipsum, needanything embarrassing hidden
                      in the middle of text.
                    </p>
                    <div>
                      <RouterLink
                        to="/blog-details"
                        class="btn btn-primary btn-rounded btn-md hover-icon"
                      >
                        <span>Viev Projects</span>
                        <i class="fas fa-arrow-right"></i>
                      </RouterLink>
                      <RouterLink
                        to="/blog-details"
                        class="btn btn-primary btn-rounded m-l15 btn-border btn-md hover-icon"
                      >
                        <span>Our Services</span>
                        <i class="fas fa-arrow-right"></i>
                      </RouterLink>
                    </div>
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="overlay-slide" data-swiper-parallax="100%">
                    <img :src="img" alt="" />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </SwiperSlide>
        <div class="swiper-pagination style-2"></div>
        <div class="slider-three-pagination">
          <div class="btn-prev swiper-button-prev3 swiper-button-white">
            <i class="las la-angle-left"></i>
          </div>
          <div class="btn-next swiper-button-next3 swiper-button-white">
            <i class="las la-angle-right"></i>
          </div>
        </div>
      </Swiper>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination, Autoplay, Parallax } from 'swiper/modules'
import slide_pic1 from '@/assets/images/main-slider/slider3/pic1.jpg'
import slide_pic2 from '@/assets/images/main-slider/slider3/pic2.jpg'
import slide_pic3 from '@/assets/images/main-slider/slider3/pic3.jpg'

export default defineComponent({
  components: { Swiper, SwiperSlide },
  setup() {
    return {
      mainSlider: [{ img: slide_pic1 }, { img: slide_pic2 }, { img: slide_pic3 }],
      module: [Navigation, Pagination, Autoplay, Parallax],
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
        renderBullet: function (index: number, className: string) {
          return '<span class="' + className + '">' + '0' + (index + 1) + '</span>'
        }
      }
    }
  }
})
</script>

<style scoped></style>
