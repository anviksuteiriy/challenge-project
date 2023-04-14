<template>
  <div class="hero">
    <div class="hero__container" :style="containerClasses">
      <div class="hero__container-text">
        <h1 class="hero__container-heading">{{ heroTitle }}</h1>
        <p class="hero__container-potential">{{ heroDesc }}</p>
        <div style="margin-top: var(--spacing-6);">
          <project-button secondary>Buat Jadwal Demo</project-button>
          <project-button style="margin-left: 10px;">Mulai Sekarang</project-button>
        </div>
      </div>
      <div class="hero__image-container">
        <img
          class="hero__intro-image"
          :style="'border-radius:' + borderRadius"
          :src="heroImage"
          alt="Header Image"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps, computed } from 'vue';
import ProjectButton from './ProjectButton.vue';

const props = defineProps({
  heroTitle: {
    type: String,
    required: true,
  },
  heroDesc: {
    type: String,
  },
  heroImage: {
    type: String,
  },
  borderRadius: {
    type: String,
    default: '0px'
  },
  justifyContent: {
    type: String,
    default: 'center'
  },
  alignItems: {
    type: String,
    default: 'flex-start'
  },
});
const containerClasses = computed(() => {
  return {
    'justify-content': props.justifyContent,
    'align-items': props.alignItems
  }
});
</script>

<style scoped>
.hero__container {
  display: flex;
  align-items: flex-start;
  background-color: var(--project-blue) !important;
  text-align: left;
}

.hero__container-para {
  font-size: 14px;
  font-weight: bold;
  line-height: 1.4;
}

.hero__container-heading {
  font-size: 48px;
  line-height: 1.2;
  font-weight: bold;
  color: var(--project-green);
  margin: 0;
}

.hero__container-potential {
  font-size: 16px;
  line-height: 1.3;
  font-weight: 400;
  color: var(--white);
}

.hero__container-text {
  width: 50%;
  margin: var(--spacing-6);
  max-width: 600px;
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}

.hero__image-container {
  width: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}

.hero__intro-image {
  max-width: 550px;
  margin: var(--spacing-6);
  max-height: 450px;
}

@media screen and (max-width: 1300px) {
  .hero__container-text {
    margin-left: 85px;
  }
}

@media screen and (max-width: 1150px) {
  .hero__container {
    align-items: center;
  }

  .hero__container-text {
    margin-left: 50px;
  }

  .hero__container-heading {
    font-size: 48px;
  }

  .hero__container-potential {
    font-size: 26px;
  }

  .hero__intro-image {
    max-width: 380px;
    margin: var(--spacing-6);
    max-height: 330px;
  }
}

@media screen and (max-width: 850px) {
  .hero__container {
    flex-direction: column;
    text-align: center;
    align-items: center;
    padding-bottom: 40px;
  }

  .hero__container-heading {
    font-size: 42px;
    padding: var(--spacing-6);
  }

  .hero__container-potential {
    padding: var(--spacing-6);
  }

  .hero__container-text {
    max-width: 100%;
  }

  .hero__container-text {
    width: 100%;
    margin: 0;
    margin-left: 0;
  }

  .hero__image-container {
    width: 100%;
  }
}

@media screen and (max-width: 500px) {

  .hero__intro-image {
    max-width: 300px;
  }

  .hero__container-heading {
    font-size: 36px;
  }

  .hero__container-potential {
    font-size: 24px;
  }

  .hero__container-text {
    margin: 0;
    min-height: 220px;
  }
}

</style>
