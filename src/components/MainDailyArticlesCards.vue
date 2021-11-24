<template>
  <div class="container">
    <p class="section_type">
      BLOG UPDATED
    </p>
    <p class="type_h2 mb-5">
      Interesting <span class="type_h2 text_primary">articles updated</span> daily
    </p>
    <div class="row row-cols-4 mb-4">
      <div class="col" v-for="article, i in articles" :key="i">
        <div class="card">
          <img :src="require('@/assets/' + article.imgSrc)" class="card-img-top" :alt="article.imgAlt">
          <div class="card-body">
            <p class="card_small_text mb-2">
              <i class="far fa-calendar"></i>
              &nbsp;
              {{article.date}}
            </p>
            <p class="card-text mb-3">{{article.title}}</p>
            <p class="card_small_text">
              {{article.preview}}
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="text-center">
      <a @click.prevent class="to_all_posts" href="#">VIEW ALL POSTS</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainDailyArticlesCards',
  data() {
    return {
      articles: [
        {
          imgSrc: 'motivation-blog-04-480x325.jpg',
          imgAlt: 'article cover',
          title: 'How to be Successful: Create A Growth Mindset For Success',
          date: 'May 13, 2020',
          preview: 'When it comes to your business or career, you want ...'
        },
        {
          imgSrc: 'motivation-blog-03-480x325.jpg',
          imgAlt: 'article cover',
          title: 'How to Build Confidence in Your Abilities',
          date: 'May 13, 2020',
          preview: 'Being self-employed and working from home, it\'s easy to get ... '
        },
        {
          imgSrc: 'motivation-blog-02-480x325.jpg',
          imgAlt: 'article cover',
          title: 'Productivity Machiine - Focus in a Distracted World',
          date: 'May 13, 2020',
          preview: 'Being a small-business owner poses a ton of challenges. We ...'
        },
        {
          imgSrc: 'motivation-blog-01-480x325.jpg',
          imgAlt: 'article cover',
          title: 'Effective Time Management Mastery - Complete Guide',
          date: 'May 13, 2020',
          preview: 'Forgive yourself for bad habits you may have started or ...'
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

.card {
    border: none;
    transition: .3s;

    &:hover {
      transform: scale(1.1);
    } 

  img {
    border-radius: 10px;
  }

  .card-text {
    color: $text_brand_secondary;
    font-weight: bold;
  }
  .card_small_text {
    font-size: $font_size_small;
    color: $text_gray;
  }
}
.to_all_posts {
  color: $text_brand_primary;
  font-weight: bold;
  text-decoration: none;
  border-bottom: 1px solid $text_brand_primary;
  padding-bottom: 5px;
}
</style>