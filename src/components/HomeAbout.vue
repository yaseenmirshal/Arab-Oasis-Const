<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-6">
        <div class="dz-media">
          <div class="img1 aos-item">
            <img src="@/assets/images/about/pic1.jpg" alt="" />
          </div>
          <div class="img2 aos-item">
            <img src="@/assets/images/about/pic2.jpg" alt="" />
          </div>
          <div class="img3 aos-item">
            <img src="@/assets/images/about/pic3.jpg" alt="" />
          </div>
        </div>
      </div>
      <div class="col-lg-6 align-self-center">
        <div class="year-exp">
          <h2 class="year aos-item counter">25</h2>
          <h4 class="text aos-item">Years Of Working Experience</h4>
        </div>
        <p class="m-b30 aos-item">
          Donec lacus velit, volutpat a consequat quis, placerat vitae massa. Nulla facilisi. Fusce
          ac odio justo. Phasellus a risus in libero feugiat aliquam quis nec metus. Sed vulputate
          bibendum nulla, eu sodales magna gravida nec. Integer sit amet sollicitudin massa, a
          blandit lectus. Vivamus lacinia justo non congue blandit.
        </p>
        <div class="accordion dz-accordion about-faq" id="aboutFaq">
          <div class="accordion-item">
            <h4 class="accordion-header">
              <RouterLink
                to="?"
                class="accordion-button"
                data-bs-toggle="collapse"
                data-bs-target="#aboutOne"
                aria-expanded="true"
                aria-controls="aboutOne"
              >
                <i class="flaticon-crane"></i>
                Construction
                <span class="toggle-close"></span>
              </RouterLink>
            </h4>
            <div
              id="aboutOne"
              class="accordion-collapse collapse show"
              aria-labelledby="aboutOne"
              data-bs-parent="#aboutFaq"
            >
              <div class="accordion-body">
                <p class="m-b0">
                  Vivamus sed eleifend diam. Proin vel orci commodo nulla viverra feugiat nec quis
                  neque.
                </p>
              </div>
            </div>
          </div>
          <div class="accordion-item">
            <h4 class="accordion-header">
              <RouterLink
                to="?"
                class="accordion-button collapsed"
                data-bs-toggle="collapse"
                data-bs-target="#aboutTwo"
                aria-expanded="false"
                aria-controls="aboutTwo"
              >
                <i class="flaticon-interior-design"></i>
                Architecture
                <span class="toggle-close"></span>
              </RouterLink>
            </h4>
            <div
              id="aboutTwo"
              class="accordion-collapse collapse"
              aria-labelledby="aboutTwo"
              data-bs-parent="#aboutFaq"
            >
              <div class="accordion-body">
                <p class="m-b0">
                  Vivamus sed eleifend diam. Proin vel orci commodo nulla viverra feugiat nec quis
                  neque.
                </p>
              </div>
            </div>
          </div>
          <div class="accordion-item">
            <h4 class="accordion-header">
              <RouterLink
                to="?"
                class="accordion-button collapsed"
                data-bs-toggle="collapse"
                data-bs-target="#aboutThree"
                aria-expanded="false"
                aria-controls="aboutTwo"
              >
                <i class="flaticon-blueprint"></i>
                Interior
                <span class="toggle-close"></span>
              </RouterLink>
            </h4>
            <div
              id="aboutThree"
              class="accordion-collapse collapse"
              aria-labelledby="aboutThree"
              data-bs-parent="#aboutFaq"
            >
              <div class="accordion-body">
                <p class="m-b0">
                  Vivamus sed eleifend diam. Proin vel orci commodo nulla viverra feugiat nec quis
                  neque.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { RouterLink } from 'vue-router'

export default defineComponent({
  name: 'homeAbout',
  setup() {
    return {}
  },
  components: { RouterLink }
})
</script>

<style scoped></style>
