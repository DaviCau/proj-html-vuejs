<template>
  <div id="app">
    <Header :info="contactInfo" :navLinks="headerLinks" />
    <Main />
    <Footer :info="contactInfo" :footerLinks="footerLinks" />
  </div>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css'
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  data() {
    return {
      contactInfo: {
        openingTime: "Open Hours: Mon - Sat - 9:00 - 18:00",
        phone: "+1 (305) 1234-5678",
        mail: "hello@example.com",
        location: "Main Avenue, 987"
      },
      headerLinks: [
        {
          name: "Home",
          url: "#"
        },
        {
          name: "About",
          url: "#"
        },
        {
          name: "Services",
          url: "#"
        },
        {
          name: "Process",
          url: "#"
        },
        {
          name: "Testimonials",
          url: "#"
        },
      ],
      footerLinks: [
        {
          section: "About",
          links: [
            {
              text: "The Company",
              url: "#"
            },
            {
              text: "Institutional",
              url: "#"
            },
            {
              text: "Social & Events",
              url: "#"
            },
            {
              text: "Innovation",
              url: "#"
            },
            {
              text: "Envoironment",
              url: "#"
            },
            {
              text: "Technology",
              url: "#"
            }
          ],
        },
        {
          section: "Transport",
          links: [
            {
              text: "Industrialized",
              url: "#"
            },
            {
              text: "Chemicals",
              url: "#"
            },
            {
              text: "Packaged Liquids",
              url: "#"
            },
            {
              text: "Construction",
              url: "#"
            },
            {
              text: "Laminated Wood",
              url: "#"
            },
            {
              text: "And others",
              url: "#"
            }
          ],
        },
        {
          section: "Support",
          links: [
            {
              text: "Responsibility",
              url: "#"
            },
            {
              text: "Terms of Use",
              url: "#"
            },
            {
              text: "About Cookies",
              url: "#"
            },
            {
              text: "Privacy Policy",
              url: "#"
            },
            {
              text: "Accessibility",
              url: "#"
            },
            {
              text: "Information",
              url: "#"
            }
          ],
        }
      ]
    }
  },
  components: {
    Main,
    Header,
    Footer
  }
}
</script>

<style lang="scss">
  @import '~bootstrap/scss/bootstrap';

  .list_none {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .full_btn {
    color: white;
    text-decoration: none;
    text-transform: uppercase;
    font-weight: bold;
    padding: 10px 20px;
    background-color: #058283;
    border-radius: 5px;

    &:hover {
      color: white;
    }
  }
  .empty_btn {
    color: white;
    text-decoration: none;
    text-transform: uppercase;
    font-weight: bold;
    padding: 10px 20px;
    background-color: transparent;
    border-radius: 5px;
    border: solid 1px #058283;

    &:hover {
      color: white;
    }
  }

  .pre_title {
    color: #018385;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: bold;
  }
  .title {
    margin: 25px 0;
    font-size: 40px;
    font-weight: bold;
  }

  .logo {
    font-weight: bold;

    span {
      color: #00a6a6;
      background-color: rgba($color: #00a6a6, $alpha: 0.2);
      padding: 10px 5px 10px 25px;
      border-top-left-radius: 20px;
      border-bottom-left-radius: 20px;
    }
  }
</style>
