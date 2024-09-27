<template>
  <div class="chess-landing-container">
    <HeaderComponent />
  </div>
</template>

<script setup>
import HeaderComponent from '../components/HeaderComponent.vue'
</script>

<style lang="scss">
.chess-landing-container {
  --clr-secondary-100: #595653;
  --clr-secondary-200: #313131;
  --clr-secondary-300: #1F1F1F;
  --clr-primary-100: #FFFFFF;


  --fs-xs: 0.75rem  // 12px
  --fs-small: 0.875rem;
  --fs-base: 1rem; // 16px
  --fs-lg: 1.125rem;
  --fs-xl: 1.25rem;
  --fs-2xl: 1.5rem; // 24px
  --fs-4xl: 2.25rem;  // 36px
  --fs-5xl: 3rem; // 48px
  --fs-6xl: 3.75rem; //60px

  @font-face {
    font-family: 'Golos text';
    src: url('../assets/fonts/GolosTextWoff2.woff2') format('woff2');
    font-display: swap;
    font-weight: 100 900;
  }

  h2, h3 {
    font-family: 'Merriweather', system-ui;
    line-height: 1.1;
  }

  h1, p, a {
    font-family: 'Golos text', sans-serif;
    line-height: 1.3;
  }
}
</style>
