<template>
  <div id="app">
    <Header />
    <main>
      <HomeView />
    </main>
    <Footer />
    <BackToTop />
    <Lightbox />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import HomeView from './views/HomeView.vue';
import Footer from './components/Footer.vue';
import BackToTop from './components/BackToTop.vue';
import Lightbox from './components/Lightbox.vue';

export default {
  name: 'App',
  components: {
    Header,
    HomeView,
    Footer,
    BackToTop,
    Lightbox
  }
};
</script>

<style>
@import './assets/css/styles.css';
</style>
