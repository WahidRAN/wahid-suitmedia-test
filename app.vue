<script setup lang="ts">
useHead({
  title: 'Monito Wahid Site',
  meta: [
    { name: 'description', content: 'This is test site for suitmedia, let me tell you all about it.' }
  ],
})

useSeoMeta({
  title: 'Monito Wahid Site',
  ogTitle: 'Monito Wahid Site',
  description: 'This is test site for suitmedia, let me tell you all about it.',
  ogDescription: 'This is test site for suitmedia, let me tell you all about it.',
})
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
