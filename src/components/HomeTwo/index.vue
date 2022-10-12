<template>
  <div>
    <!--====== PRELOADER PART START ======-->

    <!-- <div class="loader-wrap">
        <div class="preloader"><div class="preloader-close">Preloader Close</div></div>
        <div class="layer layer-one"><span class="overlay"></span></div>
        <div class="layer layer-two"><span class="overlay"></span></div>        
        <div class="layer layer-three"><span class="overlay"></span></div>        
    </div> -->

    <!--====== PRELOADER PART ENDS ======-->

    <!--====== OFFCANVAS MENU PART START ======-->
    <sidebar-home-one
      :sidebar="sidebar"
      @toggleSidebar="toggleSidebar"
      :menuItems="navs"
    />
    <!--====== OFFCANVAS MENU PART ENDS ======-->

    <!--====== APPIE HEADER PART START ======-->

    <header-home-two @toggleSidebar="toggleSidebar" :menuItems="navs" />

    <!--====== APPIE HEADER PART ENDS ======-->

    <!--====== APPIE HERO PART START ======-->

    <hero-home-two
      offer_title="SUT"
      :heading="hero_home_heading"
      :more_heading="hero_home_more_heading"
      :description="hero_home_description"
      :hero_img="hero_img"
    />

    <!--====== APPIE HERO PART ENDS ======-->

    <!--====== APPIE SERRVICE 2 PART START ======-->

    <services-home-two title="Highlights" description=" " />
    <!--====== APPIE SERRVICE 2 PART ENDS ======-->

    <!--====== APPIE ABOUT PART START ======-->

    <about-home-two
      title="สำนักวิชาวิทยาศาสตร์"
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
    />

    <!--====== APPIE ABOUT PART ENDS ======-->

    <!--====== APPIE FEATURES 2 PART START ======-->

    <feature-home-two
      title="ทำไมต้องเลือกวิทยาศาสตร์"
      more_title=" "
      description="“ Strong science background, Collaborative mindset, Innovation, Research excellence ”"
    />

    <!--====== APPIE FEATURES 2 PART ENDS ======-->

    <!--====== APPIE COUNTER PART START ======-->

    <counter-home-two
      title="ข้อมูลสถิติ"
      description="The full monty spiffing good time no biggie cack grub fantastic."
    />

    <!--====== APPIE COUNTER PART ENDS ======-->

    <!--====== APPIE VIDEO PLAYER PART START ======-->

    <video-play-home-two
      title="Watch the two-minute video to learn how."
      description="The wireless cheesed on your bike mate zonked a load of old tosh hunky dory it's all gone to pot haggle william car boot pear shaped geeza."
      videoUrl="//www.youtube.com/embed/EE7NqzhMDms?autoplay=1"
      :thumbnail="video_bg_thumb"
    />

    <!--====== APPIE VIDEO PLAYER PART ENDS ======-->

    <!--====== APPIE BLOG PART START ======-->

    <blog-home-one title="ข่าวล่าสุด" description=" " :blogs="blogs" />

    <!--====== APPIE BLOG PART ENDS ======-->

    <!--====== APPIE DOWNLOAD PART START ======-->
    <download-home-two
      title="App is available"
      more_title="for free on app store"
      description="Jolly good quaint james bond victoria sponge happy days cras arse over blatant."
    />
    <!--====== APPIE DOWNLOAD PART ENDS ======-->

    <!--====== APPIE PRICING 2 PART START ======-->

    <priceing-home-two
      title="Simple pricing for Everyone"
      description="The full monty spiffing good time no biggie cack grub fantastic."
    />

    <!--====== APPIE PRICING 2 PART ENDS ======-->

    <!--====== APPIE TESTIMONIAL 2 PART START ======-->

    <testimonial-home-two />

    <!--====== APPIE TESTIMONIAL 2 PART ENDS ======-->

    <!--====== APPIE SPONSER PART START ======-->

    <sponser-home-two
      title="Appie works best with"
      more_title="your favorite platforms"
      description="Join over 40,000 businesses worldwide."
    />

    <!--====== APPIE SPONSER PART ENDS ======-->

    <!--====== APPIE FOOTER PART START ======-->

    <footer-home-two />

    <!--====== APPIE FOOTER PART ENDS ======-->

    <!--====== APPIE BACK TO TOP PART ENDS ======-->
    <div class="back-to-top back-to-top-2">
      <a href="#"><i class="fal fa-arrow-up"></i></a>
    </div>
    <!--====== APPIE BACK TO TOP PART ENDS ======-->
  </div>
</template>

<script>
import video_bg_thumb from "@/assets/images/video-thumb-1.jpg";
// import hero_img from "@/assets/images/hero-thumb-3.png";
import hero_img from "@/assets/images/section/1.png";
import SidebarHomeOne from "../HomeOne/SidebarHomeOne.vue";
import AboutHomeTwo from "./AboutHomeTwo.vue";
import CounterHomeTwo from "./CounterHomeTwo.vue";
import DownloadHomeTwo from "./DownloadHomeTwo.vue";
import FeatureHomeTwo from "./FeatureHomeTwo.vue";
import FooterHomeTwo from "./FooterHomeTwo.vue";
import HeaderHomeTwo from "./HeaderHomeTwo.vue";
import HeroHomeTwo from "./HeroHomeTwo.vue";
import PriceingHomeTwo from "./PriceingHomeTwo.vue";
import ServicesHomeTwo from "./ServicesHomeTwo.vue";
import SponserHomeTwo from "./SponserHomeTwo.vue";
import TestimonialHomeTwo from "./TestimonialHomeTwo.vue";
import VideoPlayHomeTwo from "./VideoPlayHomeTwo.vue";

import blogOne from "@/assets/images/Highlights/4.jpg";
import blogTwo from "@/assets/images/Highlights/4.jpg";
import blogThree from "@/assets/images/Highlights/4.jpg";
import BlogHomeOne from "../HomeOne/BlogHomeOne.vue";

import axios from "axios";
// import api from "@/assets/server/api.json";
import { BASE_API_URL } from "../../constants/index.js";

export default {
  components: {
    HeaderHomeTwo,
    HeroHomeTwo,
    ServicesHomeTwo,
    AboutHomeTwo,
    FeatureHomeTwo,
    CounterHomeTwo,
    VideoPlayHomeTwo,
    DownloadHomeTwo,
    PriceingHomeTwo,
    TestimonialHomeTwo,
    SponserHomeTwo,
    FooterHomeTwo,
    SidebarHomeOne,

    BlogHomeOne,
  },
  data() {
    return {
      sidebar: false,
      navs_TH: [
        {
          name: "หน้าแรก",
          childrens: [
            {
              name: "Home 1",
              path: "/",
            },
            {
              name: "Home 2",
              path: "/home-two",
            },
            {
              name: "Home 3",
              path: "/home-three",
            },
            {
              name: "Home 4",
              path: "/home-four",
            },
            {
              name: "Home 5",
              path: "/home-five",
            },
            {
              name: "Home 6",
              path: "/home-six",
            },
            {
              name: "Home 7",
              path: "/home-seven",
            },
            {
              name: "Home 8",
              path: "/home-eight",
            },
            {
              name: "Home Dark",
              path: "/home-dark",
            },
            {
              name: "Home Rtl",
              path: "/home-rtl",
            },
          ],
        },
        {
          name: "เกี่ยวกับสำนัก",
          childrens: [
            {
              name: "About us",
              path: "/about-us",
            },
            {
              name: "About us 2",
              path: "/about-two",
            },
            {
              name: "Error",
              path: "/error",
            },
          ],
        },
        {
          name: "สาขาวิชา/สถานวิจัย",
          path: "/",
        },
        {
          name: "หลักสูตรที่เปิดสอน",
          path: "/",
        },
        {
          name: "กลุ่มงาน",
          childrens: [
            {
              name: "About us",
              path: "/about-us",
            },
            {
              name: "About us 2",
              path: "/about-two",
            },
            {
              name: "Error",
              path: "/error",
            },
          ],
        },
        {
          name: "ข่าว",
          childrens: [
            {
              name: "News",
              path: "/news",
            },
            {
              name: "Single news",
              path: "/single-news",
            },
          ],
        },
        {
          name: "อื่นๆ...",
          path: "/contact",
        },
      ],
      navs_EN: [
        {
          name: "Home",
          childrens: [
            {
              name: "Home 1",
              path: "/",
            },
            {
              name: "Home 2",
              path: "/home-two",
            },
            {
              name: "Home 3",
              path: "/home-three",
            },
            {
              name: "Home 4",
              path: "/home-four",
            },
            {
              name: "Home 5",
              path: "/home-five",
            },
            {
              name: "Home 6",
              path: "/home-six",
            },
            {
              name: "Home 7",
              path: "/home-seven",
            },
            {
              name: "Home 8",
              path: "/home-eight",
            },
            {
              name: "Home Dark",
              path: "/home-dark",
            },
            {
              name: "Home Rtl",
              path: "/home-rtl",
            },
          ],
        },
        {
          name: "About us",
          childrens: [
            {
              name: "About us",
              path: "/about-us",
            },
            {
              name: "About us 2",
              path: "/about-two",
            },
            {
              name: "Error",
              path: "/error",
            },
          ],
        },
        {
          name: "Major/Research Institute",
          path: "/",
        },
        {
          name: "Course",
          path: "/",
        },
        {
          name: "WorkGroup",
          childrens: [
            {
              name: "About us",
              path: "/about-us",
            },
            {
              name: "About us 2",
              path: "/about-two",
            },
            {
              name: "Error",
              path: "/error",
            },
          ],
        },
        {
          name: "News",
          childrens: [
            {
              name: "News",
              path: "/news",
            },
            {
              name: "Single news",
              path: "/single-news",
            },
          ],
        },
        {
          name: "other...",
          path: "/contact",
        },
      ],
      hero_img: hero_img,
      video_bg_thumb: video_bg_thumb,
      blogOne: blogOne,
      blogTwo: blogTwo,
      blogThree: blogThree,
      blogs: [
        {
          img: blogOne,
          date: "22 ตุลาคม 2020",
          category: "Saas & App",
          title: "ติดตามข่าวสาร สำนักวิชาวิทยาศาสตร์ มทส.",
        },
        {
          img: blogTwo,
          date: "22 ตุลาคม 2020",
          category: "Saas & App",
          title: "ติดตามข่าวสาร โครงการโอลิมปิกวิชาการ",
        },
        {
          img: blogThree,
          date: "22 ตุลาคม 2020",
          category: "Saas & App",
          title: "ติดตามข่าวสาร SUT Sci & Math Learning Space",
        },
      ],
      navs: [],
      hero_home_more_heading: null,
      hero_home_heading: null,
      hero_home_description: null,
    };
  },
  mounted() {
    
    document.addEventListener("scroll", this.topToBottom);

    if (!sessionStorage.type_text) {
      sessionStorage.setItem("type_text", "TH");
    }

    axios
      .get(
        BASE_API_URL +
          "&module=home&func=home_baner&text=" +
          sessionStorage.type_text
      )
      .then(
        (response) => (
          (this.hero_home_more_heading = response.data.response.home_topic),
          (this.hero_home_heading = response.data.response.home_heading),
          (this.hero_home_description = response.data.response.home_description)
        )
      );

    if (sessionStorage.type_text == "TH") {
      this.navs = this.navs_TH;
    } else {
      this.navs = this.navs_EN;
    }
  },
  methods: {
    topToBottom() {
      const result = document.querySelector(".back-to-top");
      if (
        document.body.scrollTop > window.innerHeight ||
        document.documentElement.scrollTop > window.innerHeight
      ) {
        result.style.display = "block";
      } else {
        result.style.display = "none";
      }
    },
    toggleSidebar() {
      this.sidebar = !this.sidebar;
    },
  },
};
</script>

<style></style>
