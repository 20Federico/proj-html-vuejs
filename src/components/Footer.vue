<template>
  <footer>
    <div class="container">
      <div class="d-flex justify-content-between pe-5">
        <div class="ul_box" v-for="list, i in lists" :key="i">
          <h3 :class="i === 'empty' ? 'li_empty' : ''">{{i}}</h3>
          <ul class="m-0 p-0">
            <a @click.prevent :href="listItem.href" v-for="listItem, j in list" :key="j">
              <li>
                {{listItem.text}}
              </li>
            </a>
          </ul>
        </div>
      </div>
      <div class="social_icons mb-5">
        <a @click.prevent :href="social.href" v-for="social, j in socialLinks" :key="j">
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
          {
            text: '382 NE 191st St # 87394 Miami, FL 33179-3899',
            href: '#'
          },
          {
            text: '+1(305)547-9909 (9am - 5pm EST, Monday - Friday)',
            href: '#'
          },
          {
            text: 'support@maxcoach.com',
            href: '#'
          }
        ],
        Explore: [
          {
            text: 'Start here',
            href: '#'
          },
          {
            text: 'Blog',
            href: '#'
          },
          {
            text: 'About us',
            href: '#'
          }
        ],
        empty: [
          {
            text: 'Success story',
            href: '#'
          },
          {
            text: 'Courses',
            href: '#'
          },
          {
            text: 'Contact us',
            href: '#'
          }
        ],
        Information: [
          {
            text: 'Membership',
            href: '#'
          },
          {
            text: 'Purchase guide',
            href: '#'
          },
          {
            text: 'Privacy policy',
            href: '#'
          },
          {
            text: 'Terms of service',
            href: '#'
          }
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

footer {
  padding: $padding_m 0;
  background-color: $bg_brand_secondary;
  color: $text_gray;
  position: relative;
}
.ul_box {
  flex-shrink: 0;
  padding: 15px $padding_xl 15px 0;

  .ul_box:first-of-type {
  flex-grow: 1;
  }

  h3 {
  font-size: $font_size_default;
  font-weight: bold;
  color: white;
  }

  a {
    line-height: 30px;
    font-size: 50px;
    color: $text_gray;
    text-decoration: none;
    
    &:hover {
      text-decoration: underline;
    }

    li {
    font-size: $font_size_small;
    }
  }

  li {
  }
}

.li_empty {
  color: transparent;
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