<template>
  <div class="container text-center">
    <p class="section_type">
      BEGIN YOUR JOURNEY AT MAXCOACH
    </p>
    <p class="type_h2 mb-5">Latest <span class="type_h2 text_primary">Online Courses</span></p>
    <div class="row row-cols-3 gy-5 text-start mb-5">
      <div class="col" v-for="course, i in courses" :key="i">
        <Card :courseData="course" />
      </div>
    </div>
    <button type="button" class="btn_primary">View all courses &nbsp; &nbsp; <i class="fas fa-long-arrow-alt-right"></i></button>
  </div>
</template>

<script>
import Card from './Card.vue'
export default {
  components: { Card },
  name: 'MainCoursesCard',
  data() {
    return {
      courses: [
        {
          imgSrc: 'motivation-course-06-480x298.jpg',
          imgAlt: 'course cover',
          priceInt: 30,
          priceFloats: '',
          title: 'How to be Successful: Create A Growth Mindset For Success',
          nLessons: 3,
          nStudents: 50
        },
        {
          imgSrc: 'motivation-course-05-480x298.jpg',
          imgAlt: 'course cover',
          priceInt: 30,
          priceFloats: '',
          title: 'How to Build Confidence in Your Abilities',
          nLessons: 1,
          nStudents: 50
        },
        {
          imgSrc: 'motivation-course-04-480x298.jpg',
          imgAlt: 'course cover',
          priceInt: 20,
          priceFloats: '',
          title: 'Productivity Machiine - Focus in a Distracted World',
          nLessons: 5,
          nStudents: 50
        },
        {
          imgSrc: 'motivation-course-03-480x298.jpg',
          imgAlt: 'course cover',
          priceInt: 20,
          priceFloats: '',
          title: 'Effective Time Management Mastery - Complete Guide',
          nLessons: 18,
          nStudents: 50
        },
        {
          imgSrc: 'motivation-course-02-480x298.jpg',
          imgAlt: 'course cover',
          priceInt: 25,
          priceFloats: '99',
          title: 'Body Language Secrets for Entrepreneurs',
          nLessons: 19,
          nStudents: 50
        },
        {
          imgSrc: 'motivation-course-01-480x298.jpg',
          imgAlt: 'course cover',
          priceInt: 19,
          priceFloats: '99',
          title: 'Management Skills: The Science of Leadership',
          nLessons: 17,
          nStudents: 50
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
  padding: $padding_l 0;
}
.section_type {
  font-size: $font_size_default;
  color: $text_gray;
}
</style>