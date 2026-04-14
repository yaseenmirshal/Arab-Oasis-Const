<template>
  <div
    class="modal fade"
    id="exampleModalToggle"
    aria-hidden="true"
    aria-labelledby="exampleModalToggleLabel"
    tabindex="-1"
  >
    <div class="modal-dialog modal-lg modal-dialog-centered">
      <div class="modal-content">
        <button class="mfp-close" style="top: -23px" data-bs-dismiss="modal" aria-label="Close">
          <i class="ti-close"></i>
        </button>
        <iframe
          height="100%"
          src="https://www.youtube.com/embed/sNCv3_NTNtU"
          frameborder="0"
          allowfullscreen
          allow="autoplay"
        ></iframe>
      </div>
    </div>
  </div>
  <div class="page-content bg-white">
    <MainBanner />
    <section
      class="section-full content-inner about-bx2"
      :style="`background-image: url(${backgrouBg2});`"
    >
      <HomeAbout />
    </section>
    <section class="dz-content-bx style-3">
      <CounterVideo />
    </section>
    <section class="content-inner-2">
      <div class="container">
        <div class="section-head style-1 text-center">
          <h6 class="sub-title text-primary">POPULAR SERVICES</h6>
          <h2 class="title">Our Featured Services</h2>
        </div>
        <Homeservices />
      </div>
    </section>
    <section class="content-inner-2">
      <div class="container">
        <div class="row section-head-bx align-items-center">
          <div class="col-md-8">
            <div class="section-head style-1">
              <h6 class="sub-title text-primary">OUR PORTFOLIOS</h6>
              <h2 class="title">Our Latest Projects</h2>
            </div>
          </div>
          <div class="col-md-4 text-start text-md-end mb-4 mb-md-0">
            <RouterLink to="/portfolio" class="btn-link"
              >See All Projects <i class="fas fa-plus scale08"></i
            ></RouterLink>
          </div>
        </div>
      </div>
      <OurPortfolio />
    </section>
    <section
      class="content-inner-2"
      :style="` background-image: url(${backgrouBg2});
        background-position: right bottom;
        background-size: 100%;
        background-repeat: no-repeat;`"
    >
      <Testimonial />
    </section>
    <section class="content-inner-2">
      <div class="container-fluid">
        <Testimonial2 />
      </div>
    </section>
    <HomeFaq />
    <section class="section-full dz-content-bx style-2 text-white">
      <div
        class="dz-content-inner bg-dark"
        :style="`background-image: url(${bg2_1}); background-position: center`"
      >
        <OurStrategy />
      </div>
    </section>
    <section
      class="content-inner bg-gray line-img"
      :style="` background-image: url(${backgrouBg2});
      background-position: right bottom;
      background-size: 100%;
      background-repeat: no-repeat;`"
    >
      <OurBlog />
    </section>
  </div>
</template>

<script lang="ts">

import HomeAbout from '@/components/HomeAbout.vue'
import CounterVideo from '@/components/CounterVideo.vue'
import { defineComponent, watchEffect } from 'vue'
import Homeservices from '@/components/Homeservices.vue'
import OurPortfolio from '@/components/OurPortfolio.vue'
import backgrouBg2 from '@/assets/images/background/bg2.png'
import Testimonial from '@/components/Testimonial.vue'
import Testimonial2 from '@/components/Testimonial2.vue'
import HomeFaq from '@/components/HomeFaq.vue'
import bg2_1 from '@/assets/images/background/bg2-1.png'
import OurStrategy from '@/components/OurStrategy.vue'
import OurBlog from '@/components/OurBlog.vue'
import logo from '@/assets/images/logo.png'
import logoWhite from '@/assets/images/logo-white.png'
import MainBanner from '@/components/MainBanner.vue'


export default defineComponent({
  name: 'home_',
  setup() {
    watchEffect(() => {
      setTimeout(() => {
        document.body.setAttribute('data-color', 'color_1')
        document.querySelectorAll('.header_logo').forEach((el) => {
          el.setAttribute('src', logo)
        })
        document.querySelectorAll('.header_logo2').forEach((el) => {
          el.setAttribute('src', logoWhite)
        })
      }, 10)
    })
    return { backgrouBg2, bg2_1 }
  },
  components: {
    MainBanner,
    HomeAbout,
    CounterVideo,
    Homeservices,
    OurPortfolio,
    Testimonial,
    Testimonial2,
    HomeFaq,
    OurStrategy,
    OurBlog
  }
})
</script>

<style scoped>
.section-full {
  background-image: url(../assets/images/background/bg2.png);
  background-position: right bottom;
  background-size: 100%;
  background-repeat: no-repeat;
}
.content-inner-2 {
  background-image: url(../assets/images/background/bg1.png);
  background-position: left top;
  background-size: 100%;
  background-repeat: no-repeat;
}
.modal-content {
  height: 390px;
  z-index: 99999;
}

@media screen and (max-width: 991px) {
  .modal-content {
    height: 282px;
  }
}
@media screen and (max-width: 575px) {
  .modal-content {
    height: 30vmax;
  }
}
@media screen and (max-width: 400px) {
  .modal-content {
    height: 23vmax;
  }
}
.mfp-close {
  border: none;
  outline: none;
  position: absolute;
  right: 0px;
  background-color: transparent;
  color: white;
}
</style>
