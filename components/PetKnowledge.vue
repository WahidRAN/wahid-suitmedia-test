<script setup lang="ts">
import PetKnowledgeBlog from "@/assets/json/pet-knowledge.json";

const blogData = ref(PetKnowledgeBlog);
</script>

<template>
  <AtomCardSectionWrapper title-question="You already know?" title-content="Useful Pet Knowledge">
    <AtomBlogCard
      v-for="blog in blogData"
      :key="blog.id"
      :img-src="blog.imgSrc"
      :title="blog.title"
      :desc="blog.desc"
    />
  </AtomCardSectionWrapper>
</template>
