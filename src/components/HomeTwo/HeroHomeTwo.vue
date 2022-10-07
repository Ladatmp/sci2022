<template>
      <!--====== APPIE HERO PART START ======-->
    
    <section class="appie-hero-area-2 mb-90">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-5">
                    <div class="appie-hero-content-2">
                        <span>{{offer_title}}</span>
                        <h1 class="appie-title sci-title"><h1>{{heading}}</h1> <span>{{more_heading}}</span></h1>
                        <p>{{description}}</p>
                        <form action="#">
                            <div class="input-box">
                                <input type="text" placeholder="Search...">
                                <i class="fal fa-search"></i>
                                <button><i class="fal fa-arrow-right"></i></button>
                            </div>
                        </form>
                        <div class="hero-users">
                            <!-- <img src="@/assets/images/section/hero-mans.png" alt=""> -->
                            <img class="sci-img" src="@/assets/images/sci-logo/Untitled-2-01.png" alt="">
                            <span>30k <span> Feedback</span></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="appie-hero-thumb-3 wow animated fadeInRight" data-wow-duration="2000ms" data-wow-delay="400ms">
            <img :src="hero_img" alt="">
        </div>
        <div class="hero-shape-1">
            <img src="@/assets/images/shape/shape-9.png" alt="">
        </div>
        <div class="hero-shape-2">
            <img src="@/assets/images/shape/shape-10.png" alt="">
        </div>
        <div class="hero-shape-3">
            <img src="@/assets/images/shape/shape-11.png" alt="">
        </div>
        <div class="hero-shape-4">
            <img src="@/assets/images/shape/shape-12.png" alt="">
        </div>
    </section>
    
    <!--====== APPIE HERO PART ENDS ======-->
</template>

<script>
export default {
    props: {
        offer_title:{
            type: String,
        },
        heading:{
            type: String,
        },
        more_heading:{
            type: String,
        },
        description:{
            type: String,
        },
        hero_img:{
            type: String,
        }
    }

}
</script>

<style>
    .sci-title{
        color: #ff6b58;
    }
    .sci-title h1{
        font-size: 45px;
    }

    .sci-img{
        width: 180px;
        height: 100px;
    }

</style>