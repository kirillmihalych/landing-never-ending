<template>
  <div class="main-container"></div>
</template>

<script setup></script>

<style lang="scss" scoped>
.main-container {
  --color-bg: #e9ded4;

  width: 100vw;
  height: 812px;

  @media (max-width: 1366px) {
    background: url('../assets/images/background/polotno.png'), url('../assets/images/background/small_bg.png'),
      var(--color-bg);
    background-position: bottom center, bottom right -120px, 0 0;
    background-repeat: no-repeat, no-repeat, no-repeat;
    background-blend-mode: color-burn, normal, color-burn;
    background-size: cover, auto, contain;
  }

  @media (min-width: 768px) {
    background-position: bottom center, bottom center, 0 0;
  }

  @media (min-width: 1366px) {
    background: url('../assets/images/background/polotno.png'), url('../assets/images/background/bg_desktop.png'),
      var(--color-bg);
    background-position: bottom center, top -120px left -278px, 0 0;
    background-repeat: no-repeat, no-repeat, no-repeat;
    background-blend-mode: color-burn, normal, color-burn;
    background-size: cover, auto, contain;
  }

  @media (min-width: 1920px) {
    background-position: bottom center, bottom center, 0 0;
  }
}
</style>
