<template>
  <div class="card">
    <img :src="require('@/assets/' + courseData.imgSrc)" class="card-img-top" :alt="courseData.imgAlt">
    <div class="card-body">
      <p class="text_big text_primary fw-bold mb-3">${{courseData.priceInt}}.<span>{{courseData.priceFloats.padStart(2, 0)}}</span></p>
      <p class="card-text mb-4">{{courseData.title}}</p>
      <div>
        <span class="card_small_text">
          <i class="far fa-file-alt"></i>
          {{courseData.nLessons}} Lessons  
        </span>
        <span class="card_small_text">
          <i class="far fa-user"></i>
          {{courseData.nStudents}} Students
        </span>
      </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    courseData: Object
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

  .card {
    border: none;
    transition: .3s;

    &:hover {
      -webkit-box-shadow: 0px 10px 20px 5px rgba(0,0,0,0.5); 
      box-shadow: 0px 10px 20px 5px rgba(0,0,0,0.2);
    } 
  }
  .card-text {
    color: $text_brand_secondary;
    font-weight: bold;
  }
  .card_small_text {
    font-size: $font_size_small;
    color: $text_gray;
    padding-right: 20px;
  }
</style>