<template>
<div class="my_container">
  <div class="row">
    <div class="box d-flex justify-content-center align-items-center">
      <div class="review_container text-center">
        <p class="text_primary fw-bold mb-5">REAL STORIES</p>
        <p class="heading_grey fw-bold mb-5">
          I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from syllabus. Great study portal for people like me.
        </p>
        <img src="@/assets/testimonial-avata-01.jpg" alt="testimonial avatar">
        <p class="heading_grey fw-bold">Mina Hollace</p>
        <p class="text_small">/ Freelancer</p>
      </div>
    </div>
    <div class="box">
      <img class="img_cover" src="@/assets/home-movation-testimonial-image.jpg" alt="movation testimonial image">
    </div>
  </div>
  <div class="change_review d-flex flex-column justify-content-center align-items-center">
      <i class="fas fa-caret-up"></i>
      <p class="m-0">1/4</p>
      <i class="fas fa-caret-down"></i>
    </div>
</div>
</template>

<script>
export default {
  name: 'MainReviewSection',
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.my_container {
  position: relative;
}
.img_cover {
  width: 100%;
}
.box {
  background-color: $bg_light;
  background-image: url($header_bg_img);
  width: 50%;
  padding: 0;
}
.review_container {
  width: 50%;

  img {
    border-radius: 50%;
    max-width: 70px;
    margin-bottom: 25px;
  }
  .text_small {
    color: $text_gray;
  }
}
.change_review {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 65px;
  height: 65px;
  border-radius: 50%;
  background-color: white;
  color: $text_gray;
}
</style>