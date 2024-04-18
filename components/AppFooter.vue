<script setup lang="ts">
import WranButton from "./Button.vue";
</script>

<template>
  <footer class="app-footer-wrapper">
    <div class="email-subscription-card">
      <h5>Register Now So You Don't Miss Our Programs</h5>
      <div class="email-subscription-form">
        <input type="text" placeholder="Enter your Email" />
        <WranButton>Subscribe Now</WranButton>
      </div>
    </div>
    <div class="nav-social-container">
      <nav class="menu-nav">
        <a href="#">Home</a>
        <a href="#">Category</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
      </nav>
      <ul class="menu-social">
        <img src="~/assets/icons/Facebook.svg" alt="Facebook icon" />
        <img src="~/assets/icons/Twitter.svg" alt="Twitter icon" />
        <img src="~/assets/icons/Instagram.svg" alt="Instagram icon" />
        <img src="~/assets/icons/YouTube.svg" alt="YouTube icon" />
      </ul>
    </div>
    <hr class="divider">
    <div class="footer-trademark-wrapper">
      <img src="~/assets/logos/Monito.svg" alt="Monito logo" class="footer-logo">
      <ul class="terms-policy">
        <a href="#">Terms of Service</a>
        <a href="#">Privacy Policy</a>
      </ul>
      <span class="trademark">© {{ new Date().getFullYear() }} Monito. All rights reserved.</span>
    </div>
  </footer>
</template>

<style scoped lang="scss">
.app-footer-wrapper {
  font-family: sans-serif;
  background: linear-gradient(
    102.87deg,
    var(--secondary-mon-yellow-40) 6.43%,
    var(--secondary-mon-yellow-40) 78.33%,
    #ffe7ba 104.24%
  );
  border-radius: 20px 20px 0 0;
  padding: 2.5rem 1rem 1.25rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2.5rem;
}

.email-subscription-card {
  padding: 1rem;
  background-color: var(--primary-dark-blue);
  border-radius: 1rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 100%;
  max-width: 1180px;
  h5 {
    color: var(--neutral-00);
    margin: 0;
    font-size: 1.25rem;
    font-weight: 700;
    line-height: 1.6;
  }
  .email-subscription-form {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    padding: 0.75rem;
    border-radius: 0.875rem;
    background-color: white;
  }
  input {
    max-height: 48px;
    padding: 0.875rem 1.75rem;
    border-radius: 0.5rem;
    border: 1px solid var(--neutral-40);
    font-size: 0.875rem;
    font-weight: 500;
    line-height: 1.5;
    color: var(--primary-dark-blue);
    &:focus-visible {
      outline: none;
    }
  }
}

.nav-social-container {
  display: flex;
  flex-wrap: wrap;
  gap: 1.25rem;
  width: 100%;
  max-width: 1180px;
  align-content: stretch;
  .menu-nav {
    display: flex;
    justify-content: space-between;
    width: 100%;
    font-size: 1rem;
    font-weight: 500;
    line-height: 1.5;
  }
  .menu-social {
    width: 100%;
    display: flex;
    justify-content: center;
    gap: 2.5rem;
  }
}

.divider {
  width: 100%;
  max-width: 1180px;
  margin: 0;
  border: 1px solid var(--neutral-20);
}

.footer-trademark-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  max-width: 1180px;
}

.footer-logo {
  margin-bottom: 2rem;
}

.terms-policy {
  display: flex;
  justify-content: center;
  gap: 0.75rem;
  margin-bottom: 0.5rem;
  font-size: 0.75rem;
  font-weight: 500;
  line-height: 1.5;
  color: var(--neutral-60);
}

.trademark {
  font-size: 0.625rem;
  font-weight: 400;
  line-height: 1.5;
  color: var(--neutral-60);
}

@media (min-width: 768px) {
  .app-footer-wrapper {
    padding: 5rem 2rem 2.5rem;
  }
  .email-subscription-card {
    flex-direction: row;
    align-items: center;
    gap: 1.25rem;
    padding: 2rem;
    h5 {
      width: 33%;
      font-size: 1.5rem;
      line-height: 1.5;
    }
    .email-subscription-form {
      flex-grow: 1;
      flex-direction: row;
      max-height: 72px;
      input {
        flex-grow: 1;
      }
    }
  }
  .nav-social-container {
    flex-wrap: nowrap;
    .menu-nav {
      flex-grow: 1;
      justify-content: start;
      gap: 3.75rem;
    }
    .menu-social {
      width: unset;
      img {
        width: 1.5rem;
        height: 1.5rem;
      }
    }
  }
  .footer-trademark-wrapper {
    justify-content: space-between;
    flex-direction: row;
    .footer-logo {
      order: 2;
      margin: 0;
    }
    .terms-policy {
      order: 3;
      margin: 0;
      font-size: 0.875rem;
    }
    .trademark {
      font-size: 0.875rem;
    }
  }
}
</style>
