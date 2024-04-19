<template>
  <section class="sellers-section">
    <div class="sellers-title">
      <h4>Proud to be part of <span>Pet Sellers</span></h4>
      <AtomButton outline pills>
        View all our Sellers
        <img src="~/assets/icons/chevron-right.svg" alt="chevron right icon">
      </AtomButton>
    </div>
    <div class="sellers-brand">
      <img src="~/assets/images/sheba.png" alt="sheba">
      <img src="~/assets/images/whiskas.png" alt="whiskas">
      <img src="~/assets/images/bakers.png" alt="bakers">
      <img src="~/assets/images/felix.png" alt="felix">
      <img src="~/assets/images/goodboy.png" alt="goodboy">
      <img src="~/assets/images/butchers.png" alt="butchers">
      <img src="~/assets/images/pedigree.png" alt="pedigree">
    </div>
  </section>
</template>

<style scoped lang="scss">
.sellers-section {
  display: none;
}
@media (min-width: 1200px) {
  .sellers-section {
    font-family: sans-serif;
    width: 100%;
    max-width: 1180px;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    .sellers-title {
      display: flex;
      justify-content: space-between;
      align-items: center;
      h4 {
        font-size: 1rem;
        font-weight: 500;
        line-height: 1.5;
        color: black;
        span {
          font-size: 1.5rem;
          font-weight: 700;
          color: var(--primary-dark-blue);
        }
      }
    }
    .sellers-brand {
      display: flex;
      gap: 1.25rem;
      align-items: center;
      max-height: 120px;
      img {
        object-fit: contain;
        flex-grow: 1;
      }
    }
  }
}
</style>