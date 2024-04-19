<template>
  <section class="section-banner">
    <section class="banner-wrapper">
      <div class="decor-1"></div>
      <div class="decor-2"></div>
      <img src="~/assets/images/girl-with-puppy.png" alt="girl with puppy" class="banner-image" />
      <div class="banner-text">
        <h2 class="banner-title">One more friend</h2>
        <h3 class="banner-subtitle">Thousands more fun!</h3>
        <p class="banner-desc">
          Having a pet means you have more joy, a new friend, a happy person who
          will always be with you to have fun. We have 200+ different pets that
          can meet your needs!
        </p>
        <section class="banner-action">
          <AtomButton class="intro" outline pills>
            View Intro
            <img src="~/assets/icons/play-circle.svg" alt="chevron right icon" class="play-icon">
          </AtomButton>
          <AtomButton pills>Explore Now</AtomButton>
        </section>
      </div>
    </section>
  </section>
</template>

<style scoped lang="scss">
.section-banner {
  padding: 0 1rem;
  .banner-wrapper {
    font-family: sans-serif;
    position: relative;
    width: 100%;
    height: 640px;
    max-width: 1180px;
    display: flex;
    padding: 2rem 1.25rem;
    background-color: var(--primary-dark-blue);
    border-radius: 20px;
    overflow: hidden;
    .decor-1 {
      position: absolute;
      top: -308px;
      right: -80px;
      background-color: var(--secondary-mon-yellow-40);
      border-radius: 75px;
      width: 605px;
      height: 635px;
      transform: rotate(11.41deg);
    }
    .decor-2 {
      position: absolute;
      bottom: -680px;
      left: -172px;
      background-color: var(--primary-dark-blue-80);
      border-radius: 99px;
      width: 787px;
      height: 787px;
      transform: rotate(28.25deg);
    }
    .banner-image {
      order: 2;
      height: 349px;
      position: absolute;
      bottom: 0;
      overflow: hidden;
    }
    .banner-text {
      order: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      line-height: 1.5;
      z-index: 10;
      .banner-title {
        font-size: 2.25rem;
        font-weight: 800;
        color: var(--primary-dark-blue);
      }
      .banner-subtitle {
        font-size: 1.5rem;
        font-weight: 700;
        color: var(--primary-dark-blue-80);
        margin-bottom: 0.75rem;
      }
      .banner-desc {
        font-size: 0.75rem;
        font-weight: 500;
        color: var(--neutral-80);
        text-align: center;
        margin-bottom: 2rem;
      }
      .banner-action {
        display: flex;
        gap: 1rem;
        .intro {
          display: flex;
          gap: 0.5rem;
          background-color: transparent;
          font-size: 1rem;
          .play-icon {
            width: 1.5rem;
            height: 1.5rem;
            border: 2px solid var(--primary-dark-blue);
            border-radius: 100%;
          }
        }
      }
    }
  }
}

@media (min-width: 1200px) {
  .section-banner {
    width: 100%;
    padding: 0;
    display: flex;
    justify-content: center;
    .banner-wrapper {
      height: 380px;
      flex-direction: row;
      justify-content: flex-end;
      padding: 2rem 4.75rem;
      .decor-1 {
        width: 785px;
        top: -240px;
        right: -200px;
        transform: rotate(25.23deg);
      }
      .decor-2 {
        bottom: -582px;
        transform: rotate(25.23deg);
      }
      .banner-image {
        left: 100px;
      }
      .banner-text {
        width: 100%;
        max-width: 460px;
        align-items: flex-end;
        text-align: right;
        .banner-title {
          font-size: 3.25rem;
        }
        .banner-subtitle {
          font-size: 2.25rem;
        }
        .banner-desc {
          text-align: right;
          max-width: 380px;
        }
      }
    }
  }
}
</style>