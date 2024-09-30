<template>
  <nav class="header__navbar">
    <a href="#" class="header__navbar-link">Поддержать шахматную мысль</a>
    <a href="#" class="header__navbar-link"> Подробнее <br class="header__navbar-link-br" />о турнире </a>
  </nav>
</template>

<script setup></script>

<style lang="scss" scoped>
.header__navbar {
  margin-block-start: 2rem;
  display: grid;
  gap: 0.875rem;
  text-align: center;
  font-weight: 500;

  @media (min-width: 1366px) {
    display: flex;
    gap: 1rem;
  }

  @media (min-width: 1366px) {
    margin-block-start: 2.5rem;
  }
}

.header__navbar-link {
  text-decoration: none;
  padding-block: 0.875rem;
  padding-inline: 2rem;
  border-radius: 4rem;

  @media (min-width: 768px) {
    padding-inline: 3rem;
    flex: 1 1 0px;
  }
}

.header__navbar-link:first-child {
  color: var(--clr-primary-100);
  background-color: var(--clr-secondary-300);

  @media (min-width: 1366px) {
    border: 2px solid var(--clr-secondary-300);
  }
}

.header__navbar-link:last-child {
  color: var(--clr-secondary-300);
  background-color: var(--clr-primary-100);

  @media (min-width: 1366px) {
    background-color: transparent;
    border: 2px solid var(--clr-secondary-300);
  }
}

.header__navbar-link-br {
  display: none;

  @media (min-width: 1366px) {
    display: inline-block;
  }
}
</style>
