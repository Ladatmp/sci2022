<template>
  <!--====== APPIE HEADER PART START ======-->

  <header class="appie-header-area appie-header-2-area appie-sticky">
    <div class="container-box ms-4 me-4">
      <div class="header-nav-box">
        <div class="row align-items-center">
          <div class="col-lg-2 col-md-4 col-sm-5 col-6 order-1 order-sm-1">
            <div class="appie-logo-box">
              <a href="/">
                <img
                  class="sci-logo"
                  src="@/assets/images/sci-logo/Untitled-2-01.png"
                  alt=""
                />
              </a>
            </div>
          </div>
          <div class="col-lg-9 col-md-1 col-sm-1 order-3 order-sm-2">
            <div class="appie-header-main-menu">
              <nav-items :menuItems="menuItems" :nasted="nasted" />
            </div>
          </div>
          <div class="col-lg-1 col-md-7 col-sm-6 col-6 order-2 order-sm-3">
            <div class="appie-btn-box" style="text-align: right">
              <a class="login-btn" href="#"><i class="fal fa-globe"></i> {{language}}</a>
              <!-- <a class="main-btn ml-30" href="#">Get Started</a> -->
              <div class="toggle-btn ml-30 canvas_open d-lg-none d-block">
                <i class="fa fa-bars" @click="showSidebar"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>

  <!--====== APPIE HEADER PART ENDS ======-->
</template>

<script>
import NavItems from "../NavItems.vue";
export default {
  props: {
    menuItems: {
      type: Array,
      required: true,
    },
    nasted: {
      type: Boolean,
      default: true,
    },
    language: {
      type: String,
    },
  },
  components: { NavItems },
  mounted() {
    document.addEventListener("scroll", this.stickMenu);
  },
  methods: {
    showSidebar(e) {
      this.$emit("toggleSidebar", e);
    },
    stickMenu() {
      const result = document.querySelector(".appie-sticky");
      if (
        document.body.scrollTop > 100 ||
        document.documentElement.scrollTop > 100
      ) {
        result.classList.add("sticky");
      } else {
        result.classList.remove("sticky");
      }
    },
  },
};
</script>

<style>
.sci-logo {
  width: 180px;
  height: 100px;
}
</style>
