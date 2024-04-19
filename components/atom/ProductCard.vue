<script setup lang="ts">
defineProps({
  imgSrc: String,
  title: String,
  product: String,
  size: String,
  price: String,
  currency: String,
  freebies: String
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
      <div class="content-product-profile">
        <h2>
          {{ title }}
        </h2>
        <div class="product-attr">
          <p>Product: <span>{{ product }}</span></p>
          <span v-if="size" class="dot">•</span>
          <p v-if="size">Size: <span>{{ size }}</span></p>
        </div>
      </div>
      <p class="content-price">
        {{ price }} {{ currency }}
      </p>
      <div v-if="freebies" class="content-freebies">
        <img src="~/assets/icons/gift.svg" alt="gift icon" />
        <span class="dot">•</span>
        {{ freebies }}
      </div>
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
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.25rem;
    align-items: flex-start;
    .content-product-profile {
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
      line-height: 1.5;
      h2 {
        font-size: 0.875rem;
        font-weight: 700;
        color: var(--neutral-100);
      }
      .product-attr {
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
    .content-freebies {
      width: 100%;
      display: flex;
      gap: 0.75rem;
      border-radius: 0.5rem;
      padding: 0.5rem 0.625rem 0.375rem;
      background-color: var(--secondary-mon-yellow-40);
      font-size: 0.875rem;
      font-weight: 700;
      line-height: 1.5;
      color: var(--primary-dark-blue-80);
      img {
        border-radius: 0;
      }
    }
  }
}

@media (min-width: 1200px) {
  .content-card {
    width: 20%;
    .content-meta {
      padding: 0.5rem;
      .content-product-profile {
        .product-attr {
          flex-direction: row;
          align-items: center;
          gap: 0.75rem;
          .dot {
            display: block;
          }
        }
      }
    }
  }
}
</style>
