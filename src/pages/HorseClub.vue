<template>
  <div class="horse-club-container">
    <HeaderMain />
  </div>
</template>

<script setup>
import HeaderMain from '@/components/horse_club/HeaderMain.vue'
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,600;1,600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Alegreya+Sans:wght@400;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Philosopher:wght@400;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

.horse-club-container {
  --clr-heading-1: #202020;
  --clr-heading-2: #7d808a;

  --clr-green: #008139;

  --font-size-medium-125: 1.125rem;
  --font-size-small-075: 0.5rem;
}
</style>
