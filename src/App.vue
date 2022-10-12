<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <router-view />
  </div>
</template>
<script>
export default {
  name: "APP",
  created() {
    if (sessionStorage.type_text == "TH") {
      this.navs = this.navs_TH;
      document.title = "สำนักวิชาวิทยาศาสตร์ มหาวิทยาลัยเทคโนโลยีสุรนารี.";
    } else {
      this.navs = this.navs_EN;
      document.title = "Faculty of Science, Suranaree University of Technology";
    }
  },
};
</script>

<style></style>
