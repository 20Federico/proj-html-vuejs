<template>
  <div class="container d-flex justify-content-between align-items-center">
    <div class="text_container">
      <p class="section_type">
        BOOK STORE ONLINE
      </p>
      <p class="type_h2 mb-5">
        Be Alpha With <br> 
        <span class="type_h2 text_primary">Wingman's Book</span>
      </p>
      <ul class="mb-5 p-0">
        <li class="book_feature" v-for="feature, i in booksFeatures" :key="i">
          <i class="fas fa-check"></i> 
          <span class="li_text">{{feature}}</span>
        </li>
      </ul>
      <button type="button" class="btn_primary mb-3">Get Free Ebook</button>
    </div>
    <div class="d-flex">
      <div class="my_card text-center" v-for="book, i in booksList" :key="i">
        <img class="mb-4" :src="require('@/assets/' + book.imgSrc)" alt="book cover">
        <p class="card-text">{{book.title}}</p>
        <p class="text_big text_primary fw-bold">${{book.priceInt}}.<span>{{book.priceFloats.padStart(2, 0)}}</span></p>

        <div class="buy_options">
          <ul class="m-0 p-0">
            <li v-for="opt, i in buyOptions" :key="i" :title="opt.title">
              <i :class="opt.iconClass"></i>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainTextAndCards',
  data() {
    return {
      booksFeatures: [
        'Help you understand yourself better',
        'Revealing mature tips',
        'Give the right advice',
        'Fascinating examples of alpha man'
      ],
      booksList: [
        {
          imgSrc: 'product-book-11-400x400.jpg',
          title: 'Alpha man by Maxcoach',
          priceInt: 29,
          priceFloats: ''
        },
        {
          imgSrc: 'product-book-11-400x400.jpg',
          title: 'Real man 4.0 by Maxcoach',
          priceInt: 39,
          priceFloats: ''
        }
      ],
      buyOptions: [
        {
          title: 'search',
          iconClass: 'fas fa-search'
        },
        {
          title: 'add to cart',
          iconClass: 'fas fa-shopping-cart'
        },
        {
          title: 'add favourite',
          iconClass: 'far fa-heart'
        },
        {
          title: 'info',
          iconClass: 'fas fa-signal'
        },
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
li.book_feature {
  line-height: 40px;
  color: $text_brand_primary;

  .li_text {
    color: $text_midgray;
    font-size: $font_size_small;
    padding-left: 15px;
  }
}
.my_card {
  position: relative;
  padding: 15px;

  img {
    max-width: 400px;
  }

  .card-text {
      color: $text_brand_secondary;
      font-weight: bold;
  }

  &:hover {
    .buy_options {
      display: initial;
    }
  }
}
.buy_options {

  position: absolute;
  top: 20%;
  right: 60px;
  display: none;

  li {
    border-radius: 50%;
    background-color: white;
    width: 40px;
    height: 40px;
    display: flex;
    font-size: 18px;
    justify-content: center;
    align-items: center;
    margin-bottom: 15px;
    transition: .3s;

    &:hover {
      transform: scale(1.2);
    }
  }
}
</style>