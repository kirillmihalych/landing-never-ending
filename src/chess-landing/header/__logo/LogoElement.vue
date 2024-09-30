<template>
  <header class="header__logo">
    <img src="../../assets/logo/logo.svg" alt="four knights" class="header__logo-icon" />
    <h1 class="header__logo-title">
      Клуб <br />
      четырёх коней
    </h1>
  </header>
</template>

<script setup></script>

<style lang="scss" scoped>
.header__logo {
  display: flex;
  align-items: center;
  gap: 0.25rem;
}

.header__logo-icon {
  height: 1.725rem;

  @media (min-width: 768px) {
    height: 2rem;
  }
}

.header__logo-title {
  text-transform: uppercase;
  font-weight: 700;
  color: var(--clr-secondary-100);
  font-size: 0.875rem;

  @media (min-width: 768px) {
    font-size: 1.125rem;
  }
}
</style>
