<script setup lang="ts">
defineProps({
  imgSrc: String,
  title: String,
  gene: String,
  age: String,
  price: String,
  currency: String,
});
</script>

<template>
  <div class="content-card">
    <NuxtImg
      :src="`images/${imgSrc}`"
      :alt="`${imgSrc?.split('.')[0]} icon`"
      format="webp"
      height="160px"
    />
    <section class="content-meta">
      <div class="content-pet-profile">
        <h2>
          {{ title }}
        </h2>
        <div class="pet-attr">
          <p>
            Gene: <span>{{ gene }}</span>
          </p>
          <span class="dot">•</span>
          <p>
            Age: <span>{{ age }}</span>
          </p>
        </div>
      </div>
      <p class="content-price">{{ price }} {{ currency }}</p>
    </section>
  </div>
</template>

<style scoped lang="scss">
.content-card {
  cursor: pointer;
  font-family: sans-serif;
  width: 45%;
  flex-grow: 1;
  padding: 0.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  border-radius: 0.75rem;
  box-shadow: 0px 4px 28px -2px #00000014;

  img {
    object-fit: cover;
    border-radius: 0.625rem;
  }

  .content-meta {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.25rem;
    align-items: flex-start;
    .content-pet-profile {
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
      line-height: 1.5;
      h2 {
        font-size: 0.875rem;
        font-weight: 700;
        color: var(--neutral-100);
      }
      .pet-attr {
        display: flex;
        flex-direction: column;
        gap: 0.25rem;
        p {
          font-size: 0.75rem;
          font-weight: 500;
          color: var(--neutral-60);
          span {
            font-weight: 700;
          }
        }
        .dot {
          display: none;
        }
      }
    }
    .content-price {
      font-size: 1rem;
      font-weight: 700;
      line-height: 1.5;
      color: var(--neutral-100);
    }
  }
}

@media (min-width: 1200px) {
  .content-card {
    width: 20%;
    .content-meta {
      padding: 0.5rem;
      .content-pet-profile {
        .pet-attr {
          flex-direction: row;
          align-items: center;
          .dot {
            display: block;
          }
        }
      }
    }
  }
}
</style>
