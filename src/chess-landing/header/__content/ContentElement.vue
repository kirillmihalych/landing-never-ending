<template>
  <p class="header__content">
    Оплатите взнос на телеграммы для организации <br class="header__content-br" />Международного васюкинского турнира
    по шахматам
  </p>
</template>

<script setup></script>

<style lang="scss" scoped>
.header__content {
  margin-block-start: 1.5rem;
  font-size: var(--fs-lg);
  font-weight: 400;
  color: var(--clr-secondary-200);

  @media (min-width: 768px) {
    text-align: center;
  }
}

.header__content-br {
  display: none;

  @media (min-width: 768px) {
    display: inline-block;
  }
}
</style>
