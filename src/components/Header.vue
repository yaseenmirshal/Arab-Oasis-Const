<template>
  <header class="site-header mo-left header style-1">
    <!-- Main Header -->
    <div
      :class="`sticky-header main-bar-wraper navbar-expand-lg ${headerPosition ? 'is-fixed' : ''}`"
    >
      <div class="main-bar clearfix">
        <div class="container-fluid clearfix">
          <!-- Website Logo -->
          <div class="logo-header mostion logo-dark">
            <h1>Arab Oasis Const</h1>
            <RouterLink to="/"
              ><img class="header_logo" src="@/assets/images/logo.png" alt=""
            /></RouterLink>
          </div>
          <!-- Nav Toggle Button -->
          <button
            :class="`navbar-toggler collapsed navicon justify-content-end ${
              openMenu ? 'open' : ''
            }`"
            type="button"
            @click="openMenuHeader"
          >
            <span></span>
            <span></span>
            <span></span>
          </button>
          <!-- Extra Nav -->
          <div class="extra-nav">
            <div class="extra-cell">
              <div class="extra-icon-box">
                <i class="fas fa-map-marker-alt"></i>
                <h6 class="title">Riyadh, Saudi Arabia</h6>
              </div>
              <!-- Quik Search -->
              <div class="search-inhead">
                <div class="dz-quik-search">
                  <form action="#">
                    <input
                      name="search"
                      value=""
                      type="text"
                      class="form-control"
                      placeholder="Search"
                    />
                    <span id="quik-search-remove"><i class="ti-close"></i></span>
                  </form>
                </div>
                <RouterLink class="search-link" id="quik-search-btn" to="?">
                  <i class="flaticon-loupe"></i>
                </RouterLink>
              </div>
              <div class="menu-btn navicon" @click="HeaderSidebarShow">
                <span></span>
                <span></span>
                <span></span>
              </div>
            </div>
          </div>
          <div class="header-nav navbar-collapse justify-content-end">
           
           
            <Menu />
            <div class="dz-social-icon">
              <ul>
                <li>
                  <a href="https://www.facebook.com/dexignzone/" target="_blank"
                    ><i class="fab fa-facebook-f"></i
                  ></a>
                </li>
                <li>
                  <a href="https://www.instagram.com/dexignzone/" target="_blank"
                    ><i class="fab fa-instagram"></i
                  ></a>
                </li>
                <li>
                  <a href="https://twitter.com/dexignzones/" target="_blank"
                    ><i class="fab fa-twitter"></i
                  ></a>
                </li>
                <li>
                  <a href="https://www.youtube.com/@dexignzone1723" target="_blank"
                    ><i class="fab fa-youtube"></i
                  ></a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
  <HeaderSidebar :show="sidebarShow" />
  <div class="menu-close" @click="sidebarShow = false"></div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import Menu from '@/components/Menu.vue'
import HeaderSidebar from '@/components/HeaderSidebar.vue'

export default defineComponent({
  name: 'header_',
  // eslint-disable-next-line vue/no-reserved-component-names
  components: { Menu, HeaderSidebar },
  setup() {
    const sidebarShow = ref<boolean>(false)
    const headerPosition = ref<boolean>(false)
    const openMenu = ref<boolean>(false)

    return { sidebarShow, headerPosition, openMenu }
  },

  created: function () {
    window.addEventListener('scroll', this.HeaderPosition)
  },
  unmounted: function () {
    window.removeEventListener('scroll', this.HeaderPosition)
  },
  methods: {
    HeaderSidebarShow() {
      this.sidebarShow = true
    },
    HeaderPosition() {
      const value = window.scrollY
      if (value >= 100) {
        this.headerPosition = true
      } else {
        this.headerPosition = false
      }
    },
    openMenuHeader() {
      this.openMenu = !this.openMenu
      let nav = document.querySelector('.header-nav')?.classList
      this.openMenu ? nav?.add('show') : nav?.remove('show')
    }
  }
})
</script>

<style scoped>
.logo-header {
  display: flex !important;
  align-items: center !important;
  gap: 15px;
  flex-direction: row-reverse;
  width: auto !important;
  height: auto !important;
}

.logo-header img {
  height: auto;
  width: 60px;
  flex-shrink: 0;
}

h1 {
  display: block;
  margin: 0 !important;
  padding: 0;
  font-size: 24px;
  width: auto;
  max-width: 300px;
  text-align: left;
  white-space: nowrap;
  line-height: 1.2;
}

@media only screen and (max-width: 1280px) {
  h1 {
    font-size: 20px;
    max-width: 240px;
  }
}

@media only screen and (max-width: 991px) {
  h1 {
    font-size: 18px;
    max-width: 200px;
  }
}

@media only screen and (max-width: 575px) {
  h1 {
    font-size: 16px;
    max-width: 150px;
  }
}
</style>
