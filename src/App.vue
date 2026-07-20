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


import { ref, nextTick, onMounted, onUnmounted } from 'vue';


export default {
  components : {
    Navbar,
    Hero
  },
  setup() {
    const windowWidth = ref(typeof window !== 'undefined' ? window.innerWidth : 1024)

    const handleResize = () => {
      windowWidth.value = window.innerWidth
    }

    onMounted(() => window.addEventListener('resize', handleResize))
    onUnmounted(() => window.removeEventListener('resize', handleResize))
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
    return {loading, windowWidth};
  }
}
</script>
<style>

</style>