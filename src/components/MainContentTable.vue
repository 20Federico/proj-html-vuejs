<template>
  <div class="container">
    
    <div class="first_row row align-items-center">
      <div class="col-5">
        <div class="me-5">
          <p class="text_primary fw-bold">ABOUT ME</p>
          <p class="type_h2">
            How to Be an Alpha Male: The 15 Habits of True Alphas
          </p>
        </div>
      </div>
      <div class="offset-1 col-6">
        <p class="heading_grey">
          <strong>
            Want to learn how to be <span class="text_primary">an alpha male</span>? How to be more masculine?
            How to be the man you've always wanted to be?
          </strong>
        </p>
        <p class="small_text">
          Your goal is to show the consistency of business, core values, and customer care.
          Punctuality, responsibility, individuality, accuracy, enthusiasm - you have to clearly
          explain how these qualities are applicable to your work. And the important thing is you do love what you do.
        </p>
      </div>
    </div>
    <div class="row align-items-center">
      <div class="col-7">
        <div class="imgsBox">
          <img class="backImg" src="@/assets/home-movation-video-poster-670x450.jpg" alt="video cover">
          <img class="frontImg" src="@/assets/icon-youtube-play.png" alt="youtube btn">
        </div>
      </div>
      <div class="col-5">
        <div class="p-5">
          <p class=" quote mb-5">"Every morning you have two choices: continue to sleep with your dreams, or wake up and chase them."</p>
          <img class="mb-3" src="@/assets/home-movation-shape-01.png" alt="wave icon">
          <p class="fw-bold">Kaixa Stark</p>
          <p class="small_text">WINGMAN</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainContentTable"
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
  padding: $padding_s 0;
}

.first_row {
  margin-bottom: $padding_l;
}

.imgsBox {
    position: relative;

    img {
      max-width: 100%;

      &.frontImg {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      }
      &.backImg {
        width: 100%;
      }
    }
}
.small_text {
  font-size: $font_size_small;
  color: $text_gray;
}

</style>