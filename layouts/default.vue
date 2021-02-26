<template>

  <div class="app-container">
    <Navbar />
    <div class="app-content">
      <Nuxt />
    </div>
  </div>
</template>

<script>
import Header from '../components/Header'
import SideNav from '../components/SideNav'
import Navbar from '../components/Navbar'
import Footer from '../components/Footer'

export default {
  components: {
    Header,
    SideNav,
    Navbar,
    Footer,
  },
  computed: {
    isSidebar() {
      return this.$store.getters['nav/toggleSidebar']
    },
  },

  watch: {
    $route: function () {
      if (process.client && this.isSidebar && window.innerWidth < 768) {
        this.$store.dispatch('nav/toggleSidebar')
      }
    },
  },
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.app-container{
    height: 100%;
    position: relative;
    display: grid;
    grid-template: auto 1fr auto / 1fr;
}
.app-content{
    min-height: 100vh;
    padding: 24px;
    display: grid;
    align-items: center;
    justify-items: center;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
