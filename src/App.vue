<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/Footer.vue'
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import "@/styles/variables.scss";
@import "@/styles/utilities.scss";
@import "~@fontsource/open-sans/index.css";
@import "~@fontsource/playfair-display/index.css";

* {
  font-family: $font_default;
}
#app {
  font-family: serif, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
h3 {
  font-size: $font_size_default;
}
</style>
