<template>
  <main>
    <MainDataTable />
  </main>
</template>

<script>
import MainDataTable from './MainDataTable.vue'
export default {
  components: { 
    MainDataTable 
  },
  name: "Main",
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

</style>