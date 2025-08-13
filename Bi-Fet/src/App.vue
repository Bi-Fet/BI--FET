<script>
import { RouterLink, RouterView } from 'vue-router';
import './css/main.css';
import LandingPageView from '@/views/LandingPageView.vue';

export default {
  name: 'App',
  components: {
    LandingPageView
  }
};
</script>

<template>
  <header>
    <LandingPageView />
  </header>
</template>

<style scoped>

</style>
