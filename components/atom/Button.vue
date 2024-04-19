<script setup lang="ts">
import { computed } from 'vue';

const props = defineProps({
  outline: Boolean,
  pills: Boolean
})

const buttonClasses = computed(() => ({
  "wran-button": true,
  "btn-outline": props.outline,
  "pills": props.pills
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
  padding: 0.75rem 1.75rem;
  background-color: var(--primary-dark-blue);
  color: var(--neutral-00);
  font-size: 1rem;
  line-height: 1.5;
}
.btn-outline {
  border: 1.5px solid var(--primary-dark-blue);
  background-color: white;
  font-size: 0.875rem;
  color: var(--primary-dark-blue);
}
.pills {
  border-radius: 57px;
}
</style>