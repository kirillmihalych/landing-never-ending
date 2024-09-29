<template>
  <div class="main-screen-container">
    <div class="layout-wrapper">
      <header class="logo">
        <img src="../assets/logo/logo.svg" alt="four knights" class="logo__icon" />
        <h1 class="logo__title">
          Клуб <br />
          четырёх коней
        </h1>
      </header>
      <hgroup class="heading-list">
        <h2 class="heading-list__heading">
          Превратите <br />
          уездный город
        </h2>
        <h2 class="heading-list__heading">в столицу</h2>
        <h2 class="heading-list__heading">земного шара</h2>
      </hgroup>
      <p class="text-content">
        Оплатите взнос на телеграммы для организации <br class="text-content--break-line" />Международного васюкинского
        турнира по шахматам
      </p>
      <nav class="navbar">
        <a href="#" class="navbar__link">Поддержать шахматную мысль</a>
        <a href="#" class="navbar__link"> Подробнее <br class="navbar__link--line-break" />о турнире </a>
      </nav>
    </div>
    <RunningLine />
  </div>
</template>

<script setup>
import RunningLine from '../components/RunningLine.vue'
</script>

<style lang="scss" scoped>
.main-screen-container {
  position: relative;
  background-image: url('../assets/bg/bg-chess-375.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: bottom center;
  background-attachment: fixed;

  min-height: 100vh;
  padding: 1.25rem;

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

.layout-wrapper {
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

.logo {
  display: flex;
  align-items: center;
  gap: 0.25rem;

  &__icon {
    height: 1.625rem;

    @media (min-width: 768px) {
      height: 2rem;
    }
  }

  &__title {
    text-transform: uppercase;
    font-weight: 700;
    color: var(--clr-secondary-100);
    font-size: 0.875rem;

    @media (min-width: 768px) {
      font-size: 1.125rem;
    }
  }
}

.heading-list {
  margin-block-start: 2.5rem;
  font-size: var(--fs-4xl);
  color: var(--clr-secondary-200);
  text-transform: uppercase;

  &__heading:nth-child(2) {
    text-align: center;
  }

  &__heading:last-child {
    text-align: end;
  }

  @media (min-width: 768px) {
    margin-block-start: 3.5rem;
    font-size: var(--fs-6xl);
    width: max-content;
  }
}

.text-content {
  margin-block-start: 1.5rem;
  font-size: var(--fs-lg);
  font-weight: 400;
  color: var(--clr-secondary-200);

  @media (min-width: 768px) {
    text-align: center;
  }

  &--break-line {
    display: none;

    @media (min-width: 768px) {
      display: inline-block;
    }
  }
}

.navbar {
  margin-block-start: 2rem;
  display: grid;
  gap: 0.875rem;
  text-align: center;
  font-weight: 500;

  &__link {
    text-decoration: none;
    padding-block: 0.875rem;
    padding-inline: 2rem;
    border-radius: 4rem;

    @media (min-width: 768px) {
      padding-inline: 3rem;
      flex: 1 1 0px;
    }
  }

  &__link:first-child {
    color: var(--clr-primary-100);
    background-color: var(--clr-secondary-300);

    @media (min-width: 1366px) {
      border: 2px solid var(--clr-secondary-300);
    }
  }

  &__link:last-child {
    color: var(--clr-secondary-300);
    background-color: var(--clr-primary-100);

    @media (min-width: 1366px) {
      background-color: transparent;
      border: 2px solid var(--clr-secondary-300);
    }
  }

  &__link--line-break {
    display: none;

    @media (min-width: 1366px) {
      display: inline-block;
    }
  }

  @media (min-width: 1366px) {
    display: flex;
    gap: 1rem;
  }

  @media (min-width: 1366px) {
    margin-block-start: 2.5rem;
  }
}
</style>
