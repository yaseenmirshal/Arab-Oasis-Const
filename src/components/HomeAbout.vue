<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-6">
        <div class="dz-media">
          <div class="img1 aos-item">
            <img src="https://visva-architect-interior-vuejs.netlify.app/assets/pic1-Uu0Nkczu.jpg" alt="" />
          </div>
          <div class="img2 aos-item">
            <img src="https://i.pinimg.com/736x/58/09/ee/5809ee71da5ce96842c902a193a3e497.jpg" alt="" />
          </div>
          <div class="img3 aos-item">
            <img src="https://i.pinimg.com/1200x/a2/f3/51/a2f35177f42ebb16a75ae73719567982.jpg" alt="" />
          </div>
        </div>
      </div>
      <div class="col-lg-6 align-self-center">
        <div class="year-exp">
          <h2 class="year aos-item counter">25</h2>
          <h4 class="text aos-item">Years Of Working Experience</h4>
        </div>
        <p class="m-b30 aos-item">
          At ARAB OASIS CONSTRUCTION, CONSULTANCY and ENGINEERING COMPANY. we specialize in providing our clients with the best possible services and solutions to their operations and management needs. We are a medium-sized company, which allows us to give our clients the personalized attention they deserve. Our team is committed to providing our clients with the most innovative and cost-effective solutions to their needs.
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
                Man Power
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
                Equipments
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
