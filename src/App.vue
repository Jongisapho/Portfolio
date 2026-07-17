<template>
  <div class="min-h-screen bg-white">
    <Navbar />
    <Hero />
  </div>
</template>
<script>

import AOS from 'aos';
import 'aos/dist/aos.css';
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue';


import { ref, nextTick, onMounted } from 'vue';


export default {
  components : {
    Navbar,
    Hero
  },
  setup() {
    const loading = ref(true)

    onMounted(async () => {
      await nextTick();

      AOS.init({
        duration: 800,
        once:false,
        offset:100,
        easing: 'ease-in-out'
      });

      setTimeout(() => {
        loading.value = false;
      }, 800);
    });
    return {loading};
  }
}
</script>
<style>

</style>