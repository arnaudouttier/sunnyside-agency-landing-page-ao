<template>
  <div class="site" >
    <Header/>
    <div class="site-content" >
      <Skills/>
      <Jobs/>
      <Testimonials/>
      <Gallery/>
    </div>
    <Footer/>
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  import Skills from './components/Skills.vue'
  import Jobs from './components/Jobs.vue'
  import Testimonials from './components/Testimonials.vue'
  import Gallery from './components/Gallery.vue'
  import Footer from './components/Footer.vue'

  export default {
    name: 'App',
    components: {
      Header,
      Skills,
      Jobs,
      Testimonials,
      Gallery,
      Footer
    }
  }
</script>

<style lang="scss">
@import "./src/scss/global.scss";
@import "./src/scss/variables.scss";

body{
  font-family: $main-font;
}
h1,h2,h3,h4,h5{
  font-family: $title-font;
}
</style>
