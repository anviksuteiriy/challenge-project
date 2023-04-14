<template>
  <div class="max__size-feature">
    <div class="body__container" :class="directionClass">
      <div :class="bodyContainerText">
        <h3
          class="body__container-heading"
          v-html="titleText"
        ></h3>
        <p
          v-html="titleDesc"
          class="body__container-potential"
        ></p>
      </div>
      <div style="position: relative">
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
  max-width: var(--external);
  margin: auto;
}

.body__container {
  display: flex;
  align-items: center;
  justify-content: space-around;
  margin: 50px 0;
  text-align: left;
}

.body__container-heading {
  font-size: 30px;
  line-height: 1.3;
  font-weight: bold;
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}

.body__container-potential {
  font-size: 16px;
  font-weight: 400;
  line-height: 1.4;
  font-weight: 600;
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}

.body__container-text {
  max-width: 500px;
  margin: 0 var(--spacing-6);
}

.body__container-text--center {
  max-width: 600px;
  margin: var(--spacing-6);
  text-align: center;
}


.link__container {
  display: flex;
  flex-direction: column;
}

.body__intro-image {
  max-width: 450px;
  margin: var(--spacing-6);
  animation-delay: 300ms;
  animation-duration: 1200ms;
  animation-name: fadeInUp;
  visibility: visible;
}

.body__feature-direction--row {
  flex-direction: row;
}

.body__feature-direction--row-reverse {
  flex-direction: row-reverse;
}

.body__feature-direction--column-reverse {
  flex-direction: column-reverse;
}
@media screen and (max-width: 950px) {
  .body__container {
    flex-direction: column-reverse !important;
  }

  .body__container--reverse {
    flex-direction: column-reverse !important;
  }

  .body__intro-image {
    max-width: 450px;
    margin: var(--spacing-6) 0;
  }

  .body__feature-direction--row {
    flex-direction: column;
    text-align: center;
  }

  .body__feature-direction--row-reverse {
    flex-direction: column;
    text-align: center;
  }
}

@media screen and (max-width: 500px) {
  .body__intro-image {
    max-width: 300px;
  }

  .body__container-heading {
    font-size: 24px;
  }

  .body__container-potential {
    font-size: 15px;
  }
}
</style>
