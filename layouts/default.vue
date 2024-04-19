<template>
  <div class="main-layout">
    <AppHeader />
    <slot />
    <AppFooter />
  </div>
</template>

<style scoped lang="scss">
.main-layout {
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
}

@media (min-width: 768px) {
  .main-layout {
    gap: 3.75rem;
  }
}
</style>
