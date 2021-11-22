<template>
  <header>
    <Navbar />
    <HeaderHero />
  </header>
</template>

<script>
import HeaderHero from './HeaderHero.vue'
import Navbar from './Navbar.vue'

export default {
  name: "Header",
  components: { 
    Navbar,
    HeaderHero 
  },
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

  header {
    background-color: $bg_light;
    background-image: url($header_bg_img);
  }

</style>