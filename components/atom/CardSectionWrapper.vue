<script setup lang="ts">
defineProps({
  titleQuestion: String,
  titleContent: String,
})
</script>

<template>
  <section class="section-content-wrapper">
    <div class="section-content-title">
      <h3>{{ titleQuestion }}</h3>
      <h5>{{ titleContent }}</h5>
    </div>
    <div class="section-card-wrapper">
      <slot></slot>
    </div>
    <AtomButton outline pills>
      <span>View More</span>
      <img src="~/assets/icons/chevron-right.svg" alt="chevron right icon" class="right-icon">
    </AtomButton>
  </section>
</template>

<style scoped lang="scss">
.section-content-wrapper {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  padding: 0 1rem;
  width: 100%;
  max-width: 1180px;
  justify-content: center;
}
.section-card-wrapper {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

@media (min-width: 1200px) {
  .section-content-wrapper {
    flex-direction: row;
    flex-wrap: wrap;
    align-items: flex-start;
    padding: 0;
    .right-icon {
      width: 1.25rem;
      height: 1.25rem;
    }
  }
  .section-card-wrapper {
    order: 3;
    flex-direction: row;
  }
}
</style>
