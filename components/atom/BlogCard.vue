<script setup lang="ts">
defineProps({
  title: String,
  desc: String,
  imgSrc: String,
});
</script>

<template>
  <div class="content-card">
    <NuxtImg
      :src="`images/${imgSrc}`"
      :alt="`${imgSrc?.split('.')[0]} icon`"
      format="webp"
      height="240px"
    />
    <section class="content-meta">
      <span class="content-tag">Pet knowledge</span>
      <h4 class="content-title">
        {{ title }}
      </h4>
      <p class="content-desc">
        {{ desc }}
      </p>
    </section>
  </div>
</template>

<style scoped lang="scss">
.content-card {
  cursor: pointer;
  font-family: sans-serif;
  padding: 0.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  border-radius: 0.75rem;
  box-shadow: 0px 4px 28px -2px #00000014;

  img {
    border-radius: 0.625rem;
  }

  .content-meta {
    display: flex;
    flex-direction: column;
    gap: 0.625rem;
    padding: 0.5rem;
    align-items: flex-start;
    .content-tag {
      border-radius: 1.75rem;
      padding: 0.125rem 0.625rem;
      background-color: var(--state-blue-sea);
      color: white;
      font-size: 0.625rem;
      font-weight: 700;
      line-height: 1.6;
    }
    .content-title {
      font-size: 1rem;
      font-weight: 700;
      line-height: 1.5;
      color: var(--neutral-100);
      margin-bottom: 0.375rem;
    }
    .content-desc {
      font-size: 0.875rem;
      font-weight: 400;
      line-height: 1.5;
      color: var(--neutral-80);
      overflow: hidden;
      display: -webkit-box;
      -webkit-line-clamp: 3; /* number of lines to show */
      line-clamp: 3;
      -webkit-box-orient: vertical;
    }
  }
}

@media (min-width: 768px) {
  .content-card {
    img {
      object-fit: contain;
    }
  }
}
</style>
