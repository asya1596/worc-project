<template>
  <section>
    <Hero />
    <About />
    <Services />
    <Testimonials />
    <Gallery />
    <Map />
    <Contact />
  </section>
</template>

<script>
import Hero from '../components/Hero.vue';
import About from '../components/About.vue';
import Services from '../components/Services.vue';
import Testimonials from '../components/Testimonials.vue';
import Gallery from '../components/Gallery.vue';
import Map from '../components/Map.vue';
import Contact from '../components/Contact.vue';

export default {
  name: 'HomeView',
  components: {
    Hero,
    About,
    Services,
    Testimonials,
    Gallery,
    Map,
    Contact
  }
};
</script>
