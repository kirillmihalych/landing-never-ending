<template>
  <div class="header">
    <div class="header__layout">
      <LogoElement />
      <HeadingListElement />
      <ContentElement />
      <NavbarElement />
    </div>
    <RunningLine />
  </div>
</template>

<script setup>
import LogoElement from './__logo/LogoElement.vue'
import RunningLine from '../components/RunningLine.vue'
import HeadingListElement from './__heading-list/HeadingListElement.vue'
import ContentElement from './__content/ContentElement.vue'
import NavbarElement from './__navbar/NavbarElement.vue'
</script>

<style lang="scss" scoped>
.header {
  min-height: 100vh;
  padding: 1.25rem;
  position: relative;
  background-image: url('../assets/bg/bg-chess-375.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: bottom center;
  background-attachment: fixed;

  @media (min-width: 768px) {
    background-image: url('../assets/bg/bg-chess-1366.png');
  }

  @media (min-width: 1366px) {
    background-image: url('../assets/bg/bg-chess-1920.png');
  }

  @media (min-width: 1920px) {
    background-image: url('../assets/bg/bg-chess-1920.png');
  }
}

.header__layout {
  @media (min-width: 480px) {
    width: 450px;
    margin-inline: auto;
  }

  @media (min-width: 768px) {
    width: max-content;
    margin-inline-start: 3rem;
  }

  @media (min-width: 1700px) {
    margin-inline-start: 18rem;
  }
}
</style>
