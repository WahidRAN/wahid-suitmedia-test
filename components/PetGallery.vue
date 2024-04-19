<script setup lang="ts">
import PetGallery from "@/assets/json/pet-gallery.json";

const contentData = ref(PetGallery);
</script>

<template>
  <AtomCardSectionWrapper
    title-question="What's new?"
    title-content="Take A Look At Some Of Our Pets"
    class="gallery-wrapper"
  >
    <AtomPetCard
      v-for="content in contentData"
      :key="content.id"
      :img-src="content.imgSrc"
      :title="content.title"
      :gene="content.gene"
      :age="content.age"
      :price="content.price"
      :currency="content.currency"
    />
  </AtomCardSectionWrapper>
</template>

<style lang="scss">
.gallery-wrapper {
  .section-card-wrapper {
    flex-direction: row;
    flex-wrap: wrap;
  }
}

@media (min-width: 1200px) {
  .gallery-wrapper {
    .section-card-wrapper {
      gap: 1.25rem;
    }
  }
}
</style>