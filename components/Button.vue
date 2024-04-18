<script setup lang="ts">
import { computed } from 'vue';

const buttonClasses = computed(() => ({
  "wran-button": true,
}))
</script>

<template>
  <button :class="buttonClasses">
    <slot></slot>
  </button>
</template>

<style scoped lang="scss">
.wran-button {
  cursor: pointer;
  display: flex;
  justify-content: center;
  border: none;
  border-radius: 0.5rem;
  padding: 0.875rem 1.75rem 0.625rem;
  background-color: var(--primary-dark-blue);
  color: var(--neutral-00);
  font-size: 1rem;
  line-height: 1.5;
}
</style>