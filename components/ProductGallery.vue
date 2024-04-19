<script setup lang="ts">
import ProductGallery from "@/assets/json/product-gallery.json";

const contentData = ref(ProductGallery);
</script>

<template>
  <AtomCardSectionWrapper
    title-question="Hard to choose right products for your pets?"
    title-content="Our Products"
    class="product-wrapper"
  >
    <AtomProductCard
      v-for="content in contentData"
      :key="content.id"
      :img-src="content.imgSrc"
      :title="content.title"
      :product="content.product"
      :size="content.size"
      :price="content.price"
      :currency="content.currency"
      :freebies="content.freebies"
    />
  </AtomCardSectionWrapper>
</template>

<style lang="scss">
.product-wrapper {
  &.section-content-wrapper {
    display: none;
  }
  .section-card-wrapper {
    flex-direction: row;
    flex-wrap: wrap;
  }
}

@media (min-width: 1200px) {
  .product-wrapper {
    &.section-content-wrapper {
      display: flex;
    }
    .section-card-wrapper {
      gap: 1.25rem;
    }
  }
}
</style>