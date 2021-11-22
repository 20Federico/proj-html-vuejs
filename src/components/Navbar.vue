<template>
  <nav class="py-3">
    <div class="container d-flex justify-content-between align-items-center">
      <img class="logo" src="@/assets/dark-logo.png" alt="MaxCoach Logo">
      <div class="nav_links">
        <ul>
          <li class="nav-item dropdown" v-for="link, i in navLinks" :key="i">
            <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown" href="#" role="button" aria-expanded="false">{{link.title}}</a>
            <ul class="dropdown-menu">
              <li v-for="dropdown_link, j in link.dropdown_links" :key="j"><a class="dropdown-item" :href="dropdown_link.href">{{dropdown_link.name}}</a></li>
            </ul>
          </li>
        </ul>
      </div>
      <div class="social_links">
        <i class="fab fa-twitter"></i>
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-instagram"></i>
        <i class="fab fa-linkedin"></i>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      navLinks: [
        {
          title: 'Home',
          dropdown_links: [
            {
              name: 'prova',
              href: '#'
            },
            {
              name: 'prova',
              href: '#'
            },
            {
              name: 'prova',
              href: '#'
            }
          ]
        },
        {
          title: 'Pages',
          dropdown_links: [
            {
              name: 'prova',
              href: '#'
            },
          ]
        },
        {
          title: 'Courses',
          dropdown_links: [
            {
              name: 'prova',
              href: '#'
            },
          ]
        },
        {
          title: 'Features',
          dropdown_links: [
            {
              name: 'prova',
              href: '#'
            },
          ]
        },
        {
          title: 'Blog',
          dropdown_links: [
            {
              name: 'prova',
              href: '#'
            },
          ]
        },
        {
          title: 'Shop',
          dropdown_links: [
            {
              name: 'prova',
              href: '#'
            },
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
  
  nav {
    margin-bottom: $padding_m;
  }
  
  .logo {
    width: 100px;
  }
  ul {
    margin: 0;
    
    li {
      display: inline-block;
      a {
        text-decoration: none;
        padding: 5px 25px;
        color: $text_brand_secondary;
        &:hover {
          color: $text_brand_secondary;
          text-decoration: underline;
        }
      }
    }
  }
  .social_links {
    * {
      color: $text_titles;
      width: 30px;
    }
  }
  
  i {
    color: white;
  }

</style>