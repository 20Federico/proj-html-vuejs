<template>
  <main>
    <MainOptionTagFixed />
    <MainStatsTable />
    <MainContentTable />
    <MainCoursesCards />
    <MainTextAndCards />
    <MainSponsorTable />
    <MainReviewSection />
    <MainDailyArticlesCards />
  </main>
</template>

<script>
import MainStatsTable from './MainStatsTable.vue';
import MainContentTable from './MainContentTable.vue';
import MainCoursesCards from './MainCoursesCards.vue';
import MainTextAndCards from './MainTextAndCards.vue';
import MainSponsorTable from './MainSponsorTable.vue';
import MainReviewSection from './MainReviewSection.vue';
import MainDailyArticlesCards from './MainDailyArticlesCards.vue';
import MainOptionTagFixed from './MainOptionTagFixed.vue';

export default {
  name: "Main",
  components: { 
    MainStatsTable,
    MainContentTable,
    MainCoursesCards,
    MainTextAndCards,
    MainSponsorTable,
    MainReviewSection,
    MainDailyArticlesCards,
    MainOptionTagFixed 
  }
}
</script>