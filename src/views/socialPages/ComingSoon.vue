<template>
  <div class="page-wraper bg-white">
    <div class="dz-coming-soon style-4">
      <div class="sidenav-menu">
        <div class="logo">
          <RouterLink to="/"><img src="@/assets/images/logo.png" alt="" /></RouterLink>
        </div>

        <ul class="dz-social-icon">
  <li>
    <a href="https://facebook.com/" target="_blank" rel="noopener">
      <span>Facebook</span>
    </a>
  </li>
  <li>
    <a href="https://wa.me/966563544119" target="_blank" rel="noopener">
      <span>Whatsapp</span>
    </a>
  </li>
  <li>
    <a href="https://instagram.com/" target="_blank" rel="noopener">
      <span>Instagram</span>
    </a>
  </li>
</ul>
        


      </div>
      <div class="clearfix dz-coming-bx">
        <div class="dz-content">
          <h2 class="dz-title ml2">
            <span>
</span>Our website is under construction<br /><span> check back soon!</span>
          </h2>
          <!-- <div class="countdown">
            <div class="date">
              <span class="days time">{{ days }}</span>
              <span>Days</span>
            </div>
            <div class="date">
              <span class="hours time">{{ hours }}</span>
              <span>Hours</span>
            </div>
            <div class="date">
              <span class="mins time">{{ minutes }}</span>
              <span>Minutes</span>
            </div>
            <div class="date">
              <span class="secs time">{{ seconds }}</span>
              <span>Second</span>
            </div>
          </div> -->
          <div class="dz-coming-btn">
            <RouterLink
              to="?"
              class="btn btn-primary openbtn m-r10 black btn-rounded"
              @click="openSidebar = true"
              >GET IN TOUCH</RouterLink
            >
            <RouterLink
              to="?"
              data-bs-toggle="modal"
              data-bs-target="#exampleModal"
              class="btn btn-secondary btn-rounded"
              >SUBSCRIBE NOW</RouterLink
            >
          </div>
        </div>
      </div>
      <div class="slider-box">
        <img src="https://i.pinimg.com/1200x/6d/aa/54/6daa54bf30bcada74f86cfaf5ed45563.jpg" alt="" />
      </div>
    </div>
    <div :class="`contact-sidebar ${openSidebar ? 'active' : ''}`">
      <div class="contact-box">
        <div class="logo-contact logo-dark">
          <RouterLink to="/"
            ><img class="header_logo" src="@/assets/images/logo.png" alt=""
          /></RouterLink>
        </div>
        <div class="m-b50 contact-text">
          <div class="dz-title">
            <h4>About US</h4>
            <div class="dz-separator style-1 text-primary mb-0"></div>
          </div>
          <p>
            At ARAB OASIS CONSTRUCTION, CONSULTANCY and ENGINEERING COMPANY.
             we specialize in providing our clients with the best possible services and 
             solutions to their operations and management needs.
          </p>
          <RouterLink to="" class="btn btn-primary btn-sm btn-rounded"
            >READ MORE</RouterLink
          >
        </div>
        <div class="dz-title">
          <h4>Contact Info</h4>
          <div class="dz-separator style-1 text-primary mb-0"></div>
        </div>
        <div class="icon-bx-wraper left">
          <div class="icon-md m-r20">
            <span class="icon-cell"><i class="las la-phone-volume"></i></span>
          </div>
          <div class="icon-content">
            <h5 class="tilte">Call Now</h5>
            <p class="m-b0">
              +966 56 354 4119
            </p>
          </div>
        </div>
        <div class="icon-bx-wraper left">
          <div class="icon-md m-r20">
            <span class="icon-cell"><i class="las la-envelope-open"></i></span>
          </div>
          <div class="icon-content">
            <h5 class="tilte">Email Now</h5>
            <p class="m-b0">info@araboasis-const.com</p>
          </div>
        </div>
        <div class="icon-bx-wraper left">
          <div class="icon-md m-r20">
            <span class="icon-cell"><i class="las la-map-marker"></i></span>
          </div>
          <div class="icon-content">
            <h5 class="tilte">Location</h5>
            <p class="m-b0">Riyadh, Saudi Arabia</p>
          </div>
        </div>
      </div>
    </div>
    <div class="menu-close" @click="openSidebar = false"></div>
    <div
      class="modal fade inquiry-modal"
      id="exampleModal"
      tabindex="-1"
      role="dialog"
      aria-hidden="true"
      style="margin-top: 5%"
    >
      <div class="modal-dialog modal-dialog-centered" role="document">
        <div class="inquiry-adv">
          <img src="https://i.pinimg.com/736x/d7/f7/5e/d7f75e7c2bb86a0e8d28018d2f326ff4.jpg" alt="" />
        </div>
        <div class="modal-content">
          <div class="modal-header">
            <i class="flaticon-email"></i>
            <h5 class="modal-title" id="exampleModalLongTitle">SUBSCRIBE TO OUR NEWSLATTER</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close">
              &times;
            </button>
          </div>
          <div class="modal-body">
            <div class="dzFormMsg"></div>
            <form action="script/mailchamp.php" class="dzForm" method="post">
              <div class="form-group mb-3">
                <input
                  type="text"
                  name="dzName"
                  required
                  class="form-control"
                  placeholder="YOUR NAME"
                />
              </div>
              <div class="form-group mb-3">
                <input
                  type="email"
                  name="dzEmail"
                  required
                  class="form-control"
                  placeholder="YOUR EMAIL ADDRESS"
                />
              </div>
              <div class="form-group text-center">
                <button
                  name="submit"
                  type="reset"
                  value="Submit"
                  class="btn btn-primary btn-rounded"
                >
                  SUBSCRIBE NOW
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { ref, onMounted } from 'vue'
import { RouterLink } from 'vue-router'

export default {
  name: 'comingSoon',
  components: { RouterLink },
  setup() {
    const countDownDate = new Date('Mar 5, 2024').getTime()
    let days = ref<number>(0)
    let hours = ref<number>(0)
    let minutes = ref<number>(0)
    let seconds = ref<number>(0)
    const openSidebar = ref(false)

    const updateCountdown = () => {
      const now = new Date().getTime()
      const distance = countDownDate - now
      days.value = padZero(Math.floor(distance / (1000 * 60 * 60 * 24)))
      hours.value = padZero(Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)))
      minutes.value = padZero(Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60)))
      seconds.value = padZero(Math.floor((distance % (1000 * 60)) / 1000))
      if (distance < 0) {
        clearInterval(interval)
      }
    }
    const interval = setInterval(updateCountdown, 1000)
    onMounted(updateCountdown)

    const padZero = (num: any) => {
      return num < 10 ? `0${num}` : num
    }
    return { days, hours, minutes, seconds, openSidebar }
  },

  methods: {}
}
</script>
