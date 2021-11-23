<template>
  <footer>
    <div class="container">
      <div class="d-flex justify-content-between pe-5">
        <div class="ul_box" v-for="list, i in lists" :key="i">
          <h3 :class="i === 'empty' ? 'li_empty' : ''">{{i}}</h3>
          <ul class="m-0 p-0">
            <li v-for="listItem, j in list" :key="j">
              {{listItem}}
            </li>
          </ul>
        </div>
      </div>
      <div class="social_icons mb-5">
        <a :href="social.href" v-for="social, j in socialLinks" :key="j">
          <i :class="social.class"></i>
        </a>
      </div>
      <div class="text-center">
        <p class="text_small">&copy; 2020 Maxcoach. All Rights Reserved</p>
      </div>
    </div>
    <a href="#" class="to_page_top">
      <i class="fas fa-long-arrow-alt-up"></i>
    </a>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      lists: {
        Address: [
          '382 NE 191st St # 87394 Miami, FL 33179-3899',
          '+1(305)547-9909 (9am - 5pm EST, Monday - Friday)',
          'support@maxcoach.com'
        ],
        Explore: [
          'Start here',
          'Blog',
          'About us'
        ],
        empty: [
          'Success story',
          'Courses',
          'Contact us'
        ],
        Information: [
          'Membership',
          'Purchase guide',
          'Privacy policy',
          'Terms of service'
        ]
      },
      socialLinks: [
        {
          href: '#',
          class: 'fab fa-twitter'
        },
        {
          href: '#',
          class: 'fab fa-facebook-f'
        },
        {
          href: '#',
          class: 'fab fa-instagram'
        },
        {
          href: '#',
          class: 'fab fa-linkedin'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

footer {
  padding: $padding_m 0;
  background-color: $bg_brand_secondary;
  color: $text_gray;
  position: relative;
}
h3 {
  font-size: $font_size_default;
  font-weight: bold;
  color: white;
}
li {
  line-height: 30px;
  font-size: $font_size_small;
}
.li_empty {
  color: transparent;
}
.ul_box {
  flex-shrink: 0;
  padding: 15px $padding_xl 15px 0;
}
.ul_box:first-of-type {
  flex-grow: 1;
}
.social_icons {
  a {
    color: $text_gray;
    margin-right: 25px;
    font-size: 30px;
  }
}
.to_page_top {
  position: absolute;
  bottom: 20px;
  right: 20px;
  color: white;
  width: 50px;
  height: 50px;
  background-color: $bg_brand_primary;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  font-size: 20px;
}
</style>