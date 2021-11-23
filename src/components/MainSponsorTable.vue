<template>
  <div class="container">
    <div class="row align-items-center">
      <div class="col-2 text-center" v-for="img, i in images" :key="i">
        <img :src="require('@/assets/' + img.src)" :alt="img.alt">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainDataTable",
  data() {
    return {
      images: [
        {
          src: 'client-logo-05-primary.png',
          alt: 'Itsalive logo'
        },
        {
          src: 'client-logo-06-primary.png',
          alt: 'sixbase logo'
        },
        {
          src: 'client-logo-07-primary.png',
          alt: 'nowhere famous logo'
        },
        {
          src: 'client-logo-04-primary.png',
          alt: 'pencil logo'
        },
        {
          src: 'client-logo-03-primary.png',
          alt: 'brook logo'
        },
        {
          src: 'client-logo-02-primary.png',
          alt: 'tree logo'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

  .container {
    padding: $padding_xl 0;
  }
  img {
    opacity: .4;
    transition: .5s;

    &:hover {
      opacity: 1;
    }
  }
</style>