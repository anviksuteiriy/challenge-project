<template>
  <button class="project-button" :class="buttonClass" @click="$emit('click')"
    ><slot></slot
  ></button>
</template>

<script setup>
import { defineProps, computed } from 'vue';

const props = defineProps({
  secondary: {
    type: Boolean,
  },
  tertiary: {
    type: Boolean,
  },
});
const buttonClass = computed(() => {
  return {
    'project-button--secondary': props.secondary,
    'project-button--tertiary': props.tertiary
  }
});
</script>

<style scoped>
.project-button {
  background: var(--project-green);
  color: var(--project-blue);
  border-radius: 6px;
  padding: var(--spacing-3) var(--spacing-5);
  cursor: pointer;
  border: none;
  box-sizing: border-box;
  white-space: nowrap;
  font-size: 16px;
  font-weight: 600;
  line-height: 1.4;
}

.project-button:disabled {
  cursor: not-allowed;
  opacity: var(--opacity-50);
  box-shadow: none;
}

.project-button--secondary {
  background: var(--white);
  color: var(--project-blue);
  border: 1px solid #d1d5db;
  box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.05);
}

.project-button--tertiary {
  background: var(--white);
  color: var(--tertiary);
  border: var(--border-2) solid var(--tertiary);
}
</style>
