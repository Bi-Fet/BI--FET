<template>
  <header class="landing-header">
    <Navbar />
    <Hero />
  </header>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Hero from '@/components/Hero.vue'

export default {
  name: 'LandingPageView',
  components: { 
    Navbar, 
    Hero 
  }
}
</script>

<style scoped>
.landing-header {
  position: relative; 
}

.navbar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 10;
}
</style>
