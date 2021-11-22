<template>
  <div class="container">
    <div class="row align-items-center">
      <div class="col-5">
        <div class="p-2 me-4">
          <p class="text_grey">I'M WINGMAN</p>
          <p class="type_h1">Peace On Earth A Wonderful Wish But No Way</p>
          <p class="py-3">
            Success isn't overnight. It's when everydayyou get a little better than the day before. It all adds up.
          </p>
          <button type="button" class="btn_primary">Get Started For Free &nbsp; &nbsp; <i class="fas fa-long-arrow-alt-right"></i></button>
        </div>
      </div>
      <div class="offset-1 col-6">
        <div class="imgsBox">
          <img class="backImg" src="@/assets/home-movation-shape-face-600x534.png" alt="">
          <img class="frontImg" src="@/assets/home-movation-hero-image.png" alt="Hero Img">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ColTxtImg",
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

  .imgsBox {
    position: relative;
    overflow: hidden;

    img {
      max-width: 100%;

      &.frontImg {
        position: relative;
      }
      &.backImg {
        position: absolute;
        top: 30%;
        left: 10%;
      }
    }
    
  }
</style>