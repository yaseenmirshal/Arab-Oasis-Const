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
    <CommonBanner :img="bnr6" title="Our Services" text="Our Services" />
    <section
      class="section-full content-inner"
      :style="`background-image: url(${bg2});
        background-position: right bottom;
        background-size: 100%;
        background-repeat: no-repeat;`"
    >
      <div class="container">
        <div class="row">
          <div
            class="col-lg-4 col-sm-6 aos-item"
            v-for="({ icon, title }, ind) in servicesArr"
            :key="ind"
          >
            <div class="icon-bx-wraper style-3 m-b30">
              <div class="icon-xl m-b30">
                <RouterLink to="?" class="icon-cell"><i :class="icon"></i></RouterLink>
              </div>
              <div class="icon-content">
                <h4 class="title m-b10">
                  <RouterLink to="/services-details">{{ title }}</RouterLink>
                </h4>
                <p class="m-b30">
                  Phasellus facilisis urna at ultrices egestas. Nulla mi arcu, finibus non lectus
                  non, mollis tempus enim.
                </p>
                <RouterLink
                  to="/services-details"
                  class="btn btn-primary btn-rounded btn-sm hover-icon"
                >
                  <span>Read More</span>
                  <i class="fas fa-arrow-right"></i>
                </RouterLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="dz-content-bx style-3">
      <CounterVideo />
    </section>
    <section
      class="content-inner-2"
      :style="` background-image: url(${bg2});
        background-position: right bottom;
        background-size: 100%;
        background-repeat: no-repeat;`"
    >
      <Testimonial />
    </section>
    <section
      class="content-inner-2"
      :style="`background-image: url(${bg1});
            background-position: left top;
            background-size: 100%;
            background-repeat: no-repeat;`"
    >
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
    <Brands />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CommonBanner from '@/elements/CommonBanner.vue'
import Brands from '@/elements/Brands.vue'
import CounterVideo from '@/components/CounterVideo.vue'
import Testimonial from '@/components/Testimonial.vue'
import Testimonial2 from '@/components/Testimonial2.vue'
import HomeFaq from '@/components/HomeFaq.vue'
import OurStrategy from '@/components/OurStrategy.vue'
import bnr6 from '@/assets/images/banner/bnr6.jpg'
import bg2 from '@/assets/images/background/bg2.png'
import bg1 from '@/assets/images/background/bg1.png'
import bg2_1 from '@/assets/images/background/bg2-1.png'
import { RouterLink } from 'vue-router'

export default defineComponent({
  name: 'services_',
  components: {
    CommonBanner,
    CounterVideo,
    Testimonial,
    Testimonial2,
    HomeFaq,
    OurStrategy,
    Brands,
    RouterLink
  },
  setup() {
    return {
      bnr6,
      bg2,
      bg1,
      bg2_1,
      servicesArr: [
        { icon: 'flaticon-blueprint-1', title: 'Floor Plan Design' },
        { icon: 'flaticon-crane', title: 'Construction Work' },
        { icon: 'flaticon-interior-design-1', title: 'Interior Designing' },
        { icon: 'flaticon-furniture', title: 'Furniture Production' },
        { icon: 'flaticon-home', title: 'Architecture Design' },
        { icon: 'flaticon-support', title: '24X7 Support' }
      ]
    }
  }
})
</script>
<style scoped>
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

.modal-backdrop {
  display: none !important;
}
</style>
