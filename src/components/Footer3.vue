<template>
  <footer class="site-footer style-2" id="footer">
    <div class="footer-top">
      <div class="container">
        <div class="row">
          <div class="col-lg-3 col-12 aos-item">
            <div class="widget widget_about">
              <h4 class="footer-title">CONTACT</h4>
              <div class="widget_getintuch">
                <ul>
                  <li>
                    <i class="las la-map-marker-alt"></i>
                    1247/Plot No. 39, 15th Phase, Colony, Kkatpally, Hyderabad
                  </li>
                  <li>
                    <i class="las la-phone-volume"></i>
                    +91 987-654-3210 +91 123-456-7890
                  </li>
                  <li>
                    <i class="las la-map-marker-alt"></i>
                    info@example.com info@example.com
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="offset-lg-1 col-lg-2 col-sm-4 col-6 aos-item">
            <div class="widget widget_services">
              <h4 class="footer-title">OUR LINKS</h4>
              <ul>
                <li><RouterLink to="/">Home</RouterLink></li>
                <li><RouterLink to="/about-us">About Us</RouterLink></li>
                <li><RouterLink to="/services">Services</RouterLink></li>
                <li><RouterLink to="/team">Team</RouterLink></li>
                <li><RouterLink to="/blog-grid">Blogs</RouterLink></li>
              </ul>
            </div>
          </div>
          <div class="col-lg-3 col-sm-4 col-6 aos-item">
            <div class="widget widget_services">
              <h4 class="footer-title">OUR SERVICES</h4>
              <ul>
                <li><RouterLink to="?">Strategy & Research</RouterLink></li>
                <li><RouterLink to="?">Web Development</RouterLink></li>
                <li><RouterLink to="?">Web Solution</RouterLink></li>
                <li><RouterLink to="?">Digital Marketing</RouterLink></li>
                <li><RouterLink to="?">App Design</RouterLink></li>
              </ul>
            </div>
          </div>
          <div class="col-lg-3 col-sm-4 col-6 aos-item">
            <div class="widget widget_services">
              <h4 class="footer-title">OTHER LINKS</h4>
              <ul>
                <li><RouterLink to="?">FAQ</RouterLink></li>
                <li><RouterLink to="?">Portfolio</RouterLink></li>
                <li><RouterLink to="?">Privacy Policy</RouterLink></li>
                <li><RouterLink to="?">Terms & Condition</RouterLink></li>
                <li><RouterLink to="?">Support</RouterLink></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- footer bottom part -->
    <div class="footer-bottom">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-md-6 text-center text-md-start">
            <span class="copyright-text"
              >Copyright © {{ new Date().getFullYear() }}
              <a href="https://dexignzone.com/" class="text-primary" target="_blank">DexignZone</a>
              All rights reserved.</span
            >
          </div>
          <div class="col-md-6 text-center text-md-end">
            <ul class="footer-link d-inline-block">
              <li><RouterLink to="?">About</RouterLink></li>
              <li><RouterLink to="?">Help Desk</RouterLink></li>
              <li><RouterLink to="?">Privacy Policy</RouterLink></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'footer_',
  setup() {
    return {}
  }
})
</script>

<style scoped></style>
