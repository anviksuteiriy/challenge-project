<template>
  <NavigationComponent />
  <HeroComponent
    :heroTitle="pageHeroTitle"
    :heroDesc="pageHeroDesc"
    :heroImage="heroImages"
    borderRadius="6px"
    alignItems="center"
  />
  <SubComponent />
  <BigOppurtunitiesComponent />
  <CarouselComponent />
  <BrandComponent />
  <AccordianComponent />
  <AdvertiseComponent />
  <FooterComponent />
</template>

<script setup>
import { ref } from 'vue';
import NavigationComponent from './components/NavigationComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import SubComponent from './components/SubComponent.vue';
import BigOppurtunitiesComponent from './components/BigOppurtunitiesComponent.vue';
import CarouselComponent from './components/CarouselComponent.vue';
import BrandComponent from './components/BrandComponent.vue';
import AccordianComponent from './components/AccordianComponent.vue';
import AdvertiseComponent from './components/AdvertiseComponent.vue';
import FooterComponent from './components/FooterComponent.vue';


const pageHeroTitle = ref('Tempat Bisnis  Mulai Toko Online-mu, Pegang Kendali untuk Berkembang');
const pageHeroDesc = ref('Dengan website toko online yang lengkap & praktis, tidak ada lagi penghalang untuk optimalkan peluang pertumbuhan bisnismu.');
const heroImages = ref('https://lummoshop.co.id/wp-content/uploads/2022/01/image-header-1.png');
</script>

<style>
#app {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  margin: 0;
}

@font-face {
  font-family: 'Calibre';
  src: url('~@/assets/fonts/CalibreWeb-Regular.eot'),
    url('~@/assets/fonts/CalibreWeb-Regular.woff') format('woff'),
    url('~@/assets/fonts/CalibreWeb-Regular.woff2') format('woff2');
  font-weight: normal;
}
@font-face {
  font-family: 'Calibre';
  src: url('~@/assets/fonts/CalibreWeb-Bold.eot'),
    url('~@/assets/fonts/CalibreWeb-Bold.woff') format('woff'),
    url('~@/assets/fonts/CalibreWeb-Bold.woff2') format('woff2');
  font-weight: bold;
}
@font-face {
  font-family: 'Calibre';
  src: url('~@/assets/fonts/CalibreWeb-Semibold.eot'),
    url('~@/assets/fonts/CalibreWeb-Semibold.woff') format('woff'),
    url('~@/assets/fonts/CalibreWeb-Semibold.woff2') format('woff2');
  font-weight: 600;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0,30%,0)
  }

  to {
    opacity: 1;
    transform: none
  }
}
</style>
