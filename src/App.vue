<script setup>
  import Hero from '@/components/Hero.vue'
  import Intro from '@/components/Intro.vue'
  import OpeningHours from '@/components/OpeningHours.vue'
  import CocktailsMenu from './components/CocktailsMenu.vue';
  import Contact from './components/Contact.vue';
  import Footer from './components/Footer.vue';
</script>

<template>
  <Hero />
  <Intro />
  <div class="images">
    <img src="@/assets/info-image1.jpg" alt="">
    <img src="@/assets/info-image2.jpg" alt="">
    <img class="O" src="./components/icons/O.svg" alt="">
  </div>
  <OpeningHours />
  <CocktailsMenu />
  <Contact />
  <Footer />
</template>

<style scoped>
  .images {
    display: flex;
    position: relative;
  }
  .images img {
    width: 50%;
  }

  .images .O {
    position: absolute;
    top: 40%;
    max-width: 300px;
    right: 0;
    height: 800px;
  }

  @media (max-width: 1000px) {
    .images .O {
      height: 600px;
      top: 30%;
    }
  }
  @media (max-width: 500px) {
    .images .O {
      height: 400px;
      top: 10%;
    }
  }

  @media (max-width: 600px) {
    .images {
      flex-direction: column;
    }
    .images img {
      width: 100%;
    }

    
  }
</style>
