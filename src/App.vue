<template>
  <div id="app">
    <Header :navLinks="headerLinks" />
    <Main />
    <Footer />
  </div>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css'
import Main from './components/Main.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  data() {
    return {
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

</style>
