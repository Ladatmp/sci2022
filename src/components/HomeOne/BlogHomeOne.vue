<template>
      <!--====== APPIE BLOG PART START ======-->
    
    <section class="appie-services-2-area pt-90 pb-95">
        <div class="container">
            <div class="row align-items-end">
                <div class="col-lg-10 col-md-8">
                    <div class="appie-section-title">
                        <h3 class="appie-title">{{title}}</h3>
                        <p>{{description}}</p>
                    </div>  
                </div>
                <div class="col-lg-2 col-md-4">
                    <div class="appie-section-title text-right">
                        <a class="main-btn" href="#">View all <i class="fal fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
            <div class="row">
                <div v-for="(blog,index) in blogs" :key="index" class="col-lg-4 col-md-6">
                    <div class="appie-blog-item mt-30 wow animated fadeInUp" data-wow-duration="3000ms" data-wow-delay="200ms">
                        <div class="thumb">
                            <img :src="blog.img" :alt="blog.title">
                        </div>
                        <div class="content">
                            <div class="blog-meta">
                                <ul>
                                    <li>{{blog.date}}</li>
                                    <li><a href="#">Saas & App</a></li>
                                </ul>
                            </div>
                            <h3 class="title"><router-link to="/single-news">{{blog.title}}</router-link></h3>
                            <router-link to="/single-news">Learn More <i class="fal fa-arrow-right"></i></router-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!--====== APPIE BLOG PART ENDS ======-->
</template>

<script>
export default {
    props:{
        title:{
            type:String,
        },
        description:{
            type:String,
        },
        blogs:{
            type:Array,
            default:()=>{
                return []
            }
        }
    }

}
</script>

<style>
.appie-blog-item .content .title{
    font-family: 'Prompt';
}
</style>