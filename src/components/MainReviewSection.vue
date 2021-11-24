<template>
<div class="my_container">
  <div class="row">
    <div class="box d-flex justify-content-center align-items-center">
      <div class="review_container text-center">
        <p class="text_primary fw-bold mb-5">REAL STORIES</p>
        <p class="heading_grey fw-bold mb-5">{{reviews[activeReview].text}}</p>
        <img :src="require('@/assets/' + reviews[activeReview].profileImgSrc)" alt="testimonial avatar">
        <p class="heading_grey fw-bold">{{reviews[activeReview].name}}</p>
        <p class="text_small">/ {{reviews[activeReview].career}}</p>
      </div>
    </div>
    <div class="box">
      <img class="img_cover" src="@/assets/home-movation-testimonial-image.jpg" alt="movation testimonial image">
    </div>
  </div>
  <div class="change_review d-flex flex-column justify-content-center align-items-center">
      <div @click="prevReview()" class="icon_box">
        <i class="fas fa-caret-up"></i>
      </div>
      <p class="m-0">{{activeReview + 1}}/{{reviews.length}}</p>
      <div class="icon_box" @click="nextReview()">
        <i class="fas fa-caret-down"></i>
      </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'MainReviewSection',
  data() {
    return {
      activeReview: 2,
      reviews: [
        {
          text: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from syllabus. Great study portal for people like me.',
          profileImgSrc: 'testimonial-avata-02.jpg',
          name: 'Mina Hollace',
          career: 'Freelancer'
        },
        {
          text: 'free to learn at my own pace, follow my own schedule syllabus. Great study portal for people like me.',
          profileImgSrc: 'testimonial-avata-01.jpg',
          name: 'Tom Clancy',
          career: 'Employee'
        },
        {
          text: 'Learn am free to at my own pace, follow my own schedule and choose the subject I want to learn from syllabus. Great study portal.',
          profileImgSrc: 'testimonial-avata-03.jpg',
          name: 'George Crumble',
          career: 'Freelancer'
        },
        {
          text: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from syllabus. Great study portal for people like me. I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from syllabus.',
          profileImgSrc: 'testimonial-avata-04.jpg',
          name: 'Mark Lexus',
          career: 'Employee'
        }
      ]
    }
  },
  methods: {
    prevReview() {
      if (this.activeReview < (this.reviews.length - 1)) {
        this.activeReview++
      } else {
        this.activeReview = 0
      }
      return this.activeReview
    },
    nextReview() {
      if (this.activeReview > 0) {
        this.activeReview--
      } else {
        this.activeReview = (this.reviews.length - 1)
      }
      return this.activeReview
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.my_container {
  position: relative;
  overflow: hidden;
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