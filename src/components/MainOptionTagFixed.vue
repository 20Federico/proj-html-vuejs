<template>
  <div class="opt_tag_box">
    <a @click.prevent :title="opt.title" :href="opt.href" v-for="opt, i in optList" :key="i">
      <i :class="opt.iconClass"></i>
    </a>
  </div>
</template>

<script>
export default {
  name: 'MainOptionTagFixed',
  data() {
    return {
      optList: [
        {
          title: 'courses',
          href: '#',
          iconClass: 'fas fa-chalkboard'
        },
        {
          title: 'non so cosa sia sta roba',
          href: '#',
          iconClass: 'fab fa-gg-circle'
        },
        {
          title: 'books',
          href: '#',
          iconClass: 'fas fa-book'
        },
        {
          title: 'cart',
          href: '#',
          iconClass: 'fas fa-shopping-cart'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

  .opt_tag_box {
    position: fixed;
    top: 25%;
    right: 0;
    border-top-left-radius: 7px;
    border-bottom-left-radius: 7px;
    display: flex;
    flex-direction: column;
    align-items: center;
    -webkit-box-shadow: 5px 2px 15px 5px rgba(0,0,0,0.2); 
    box-shadow: 5px 2px 15px 5px rgba(0,0,0,0.2);
    transition: .5s;

    &:hover {
      transform: scale(1.2);
    }

    a {
      padding: 5px;
      font-size: $font_default;
      color: $text_titles;
      transition: .3s;

      &:hover {
        transform: scale(1.2);
      }
    }
  }
</style>