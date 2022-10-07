<template>
  <!--====== APPIE FEATURES 2 PART START ======-->

  <section class="appie-features-area-2 pt-90 pb-100" id="features">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-12">
          <div class="appie-section-title appie-section-title-2 text-center">
            <h3 class="appie-title">
              {{ title }}<br />
              {{ more_title }}
            </h3>
            <p>{{ description }}</p>
          </div>
        </div>
      </div>
      <div class="row mt-30 align-items-center">
        <div class="col-lg-6">
          <div class="appie-features-boxes">
            <div class="appie-features-box-item">
              <h4 class="title">ช่วยแก้ไขปัญหา</h4>
              <p>
                วิทยาศาสตร์ช่วยแก้ไขปัญหาอย่างไร? ยกตัวอย่างสถานการณ์ COVID-19
                วิทยาศาสตร์มีส่วนสำคัญอย่างมากในการช่วยแก้ไขปัญหาการระบาดของโรคด้วยการสร้างนวัตกรรมเพื่อตอบโจทย์การแก้ไขปัญหา
              </p>
            </div>
            <div class="appie-features-box-item item-2">
              <h4 class="title">เป็นส่วนสำคัญของหลายอาชีพ</h4>
              <p>
                วิทยาศาสตร์เป็นพื้นฐานสำคัญของหลากหลายอาชีพมากมาย
                ซึ่งล้วนแล้วใช้วิทยาศาสตร์เป็นหัวใจหลักในการประกอบอาชีพและการใช้ชีวิตประจำวันตั้งแต่ตื่นนอนจนถึงเข้านอน
              </p>
            </div>
            <div class="appie-features-box-item item-3">
              <h4 class="title">ทันสมัยไม่ตกยุค</h4>
              <p>
                ในยุคที่เต็มไปด้วยเทคโนโลยีและข้อมูลอย่างมหาศาล
                วิทยาศาสตร์มีบทบาทสำคัญต่อโลกปัจจุบันและอนาคตอยู่เสมอ
                วิทยาศาสตร์เป็นส่วนสำคัญที่ทำให้เกิดการพัฒนาเทคโนโลยีที่มีประสิทธิภาพและส่งเสริมคุณภาพชีวิตสูงสุดแก่มนุษย์
              </p>
            </div>
          </div>
        </div>
        <div class="col-lg-6">
          <div
            class="appie-features-thumb wow animated fadeInRight"
            data-wow-duration="2000ms"
            data-wow-delay="200ms"
          >
            <img src="@/assets/images/section/DSC6209.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="features-shape-1">
      <img src="@/assets/images/shape/shape-15.png" alt="" />
    </div>
    <div class="features-shape-2">
      <img src="@/assets/images/shape/shape-14.png" alt="" />
    </div>
    <div class="features-shape-3">
      <img src="@/assets/images/shape/shape-13.png" alt="" />
    </div>
  </section>

  <!--====== APPIE FEATURES 2 PART ENDS ======-->
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
    more_title: {
      type: String,
    },
    description: {
      type: String,
    },
  },
};
</script>

<style></style>
