<template>
  <main>
    <MainStatsTable />
    <MainContentTable />
    <MainSponsorTable />
  </main>
</template>

<script>
import MainContentTable from './MainContentTable.vue';
import MainSponsorTable from './MainSponsorTable.vue';
import MainStatsTable from './MainStatsTable.vue';

export default {
  components: { 
    MainStatsTable,
    MainContentTable,
    
    MainSponsorTable 
  },
  name: "Main",
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

</style>