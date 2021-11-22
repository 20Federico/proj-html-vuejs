<template>
  <header>
    <Navbar />
  </header>
</template>

<script>
import Navbar from './Navbar.vue'
export default {
  name: "Header",
  components: { 
    Navbar 
  },
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

</style>