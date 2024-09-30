<template>
  <hgroup class="header__heading-list">
    <h2 class="header__heading-list-item">
      Превратите <br />
      уездный город
    </h2>
    <h2 class="header__heading-list-item">в столицу</h2>
    <h2 class="header__heading-list-item">земного шара</h2>
  </hgroup>
</template>

<script setup></script>

<style lang="scss" scoped>
.header__heading-list {
  margin-block-start: 2.5rem;
  font-size: var(--fs-4xl);
  color: var(--clr-secondary-200);
  text-transform: uppercase;

  @media (min-width: 768px) {
    margin-block-start: 3.5rem;
    font-size: var(--fs-6xl);
    width: max-content;
  }
}

.header__heading-list-item:nth-child(2) {
  text-align: center;
}

.header__heading-list-item:last-child {
  text-align: end;
}
</style>
