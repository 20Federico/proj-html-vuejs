<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import "@fortawesome/fontawesome-free/js/all.js";
import 'bootstrap';
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
@import "~bootstrap/scss/bootstrap";
@import "@/styles/variables.scss";
@import "@/styles/utilities.scss";
@import "~@fontsource/open-sans/index.css";
@import "~@fontsource/playfair-display/index.css";

* {
  font-family: $font_default;
  font-size: $font_size_default;
}
img,
button {
  @include no_select;
}
ul {
  list-style: none;
}
#app {
  font-family: serif, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
h3 {
  font-size: $font_size_default;
}
.change_review {
  @include no_select;
}
</style>
