<template>
  <div class="max__size-feature">
    <div class="body__container" :class="directionClass">
      <div :class="bodyContainerText">
        <div class="body__container-caption" v-html="captionText"></div>
        <div
          class="body__container-heading"
          v-html="titleText"
        ></div>
        <p
          v-html="titleDesc"
          class="body__container-potential"
        ></p>
      </div>
      <div>
        <slot>
          <img
            class="body__intro-image"
            :src="imageUrl"
          />
        </slot>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps, computed } from 'vue';

const props = defineProps({
  captionText: {
    type: String,
  },
  titleText: {
    type: String,
  },
  titleDesc: {
    type: String,
  },
  imageUrl: {
    type: String,
  },
  flexDirection: {
    type: String,
    default: 'row'
  }
});
const directionClass = computed(() => {
  if (props.flexDirection === 'row') {
    return 'body__feature-direction--row body__container'
  } else if (props.flexDirection === 'column-reverse') {
    return 'body__feature-direction--column-reverse body__container--reverse'
  } else {
    return 'body__feature-direction--row-reverse body__container'
  }
});
const bodyContainerText = computed(() => {
  if (props.flexDirection === 'column-reverse') {
    return 'body__container-text--center'
  } else {
    return 'body__container-text'
  }
});
</script>

<style scoped>
.max__size-feature {
  width: 50%;
}

.body__container {
  display: flex;
  align-items: center;
  justify-content: space-around;
  margin: 20px 0;
  text-align: center;
}
.body__container-caption {
  text-align: center;
  font-weight: bold;
  margin-bottom: 20px;
  font-size: 14px;
}
.body__container-heading {
  font-size: 30px;
  line-height: 1.2;
  font-weight: bold;
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}

.body__container-potential {
  font-size: 15px;
  font-weight: 600;
  line-height: 1.4;
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}

.far {
  color: var(--rumie-web-yellow);
  margin-right: var(--spacing-2);
}

.body__container-text {
  max-width: 500px;
  margin: 0 var(--spacing-6);
}

.body__container-text--center {
  max-width: 400px;
  margin: var(--spacing-2);
  text-align: center;
}


.body__intro-image {
  max-width: 350px;
  margin: var(--spacing-2);
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}
.body__feature-direction--row-reverse {
  flex-direction: row-reverse;
}

.body__feature-direction--column-reverse {
  flex-direction: column-reverse;
}

.mighty__donate--button {
  padding: 10px 45px !important;
}

@media screen and (max-width: 950px) {
  .max__size-feature {
    width: 100%;
  }
  .body__container {
    flex-direction: column-reverse !important;
  }

  .body__container--reverse {
    flex-direction: column-reverse !important;
  }

  .body__intro-image {
    max-width: 350px;
    margin: var(--spacing-2) 0;
  }

  .body__intro-home {
    display: flex;
    justify-content: center;
    margin-top: var(--spacing-20);
  }

  .body__feature-direction--row {
    flex-direction: column;
    text-align: center;
  }

  .body__feature-direction--row-reverse {
    flex-direction: column;
    text-align: center;
  }

  .social__links {
    margin: 0 auto;
  }
}

@media screen and (max-width: 500px) {
  .body__intro-image {
    max-width: 300px;
  }

  .body__intro-home {
    max-width: 300px;
    margin: var(--spacing-6);
  }

  .body__overlay-image {
    position: absolute;
    right: 25px;
    max-width: 280px;
    top: 60px;
  }

  .body__container-heading {
    font-size: 24px;
  }

  .feature__link {
    font-size: 14.4px;
  }
  .location__name,
  .reviewers__name {
    font-size: 14.4px;
  }
}
</style>
