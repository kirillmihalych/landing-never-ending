<template>
  <div class="cards-layout-container">
    <h2 class="title">Cards</h2>
    <ul class="cards-layout">
      <li class="card-item" v-for="number in 8" :key="number">
        <header>
          <img src="../assets/images/скрины_жпеги/жпег_скрин_5.jpg" alt="жпег_скрин_5" />
        </header>
        <div class="card-item__content-container">
          <p class="card-item__image-text">Скринчик из ведьмака какой-то</p>
          <h3 class="card-item__title">Геральт на плотве стоит у обрыва</h3>
          <p class="card-item__text-content">
            Выставка катеров и яхт Sochi Boat Show состоится с 19 по 29 июля 2020 года в нашем яхт-клубе. В программе
            будет демонстрация и тест-драйвы водомоторной
          </p>
          <footer class="card-footer">
            <div class="card-footer__creator">
              <img
                src="../assets/images/скрины_жпеги/жпег_скрин_7.jpg"
                alt="жпег_скрин_7"
                class="card-footer__avatar"
              />
              <div>
                <p class="card-footer__name">Антон Цинтрийский</p>
                <p class="card-footer__date">05.05.1995</p>
              </div>
            </div>
            <a href="#">
              <img src="../assets/images/icons/share_icon.png" alt="btn-icon" class="card-footer__btn" />
            </a>
          </footer>
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@0,100..900;1,100..900&display=swap');

.cards-layout-container {
  --ff: 'Noto Sans', system-ui;
  --clr-primary: #283c54;
  --clr-secondary: #163152;

  font-family: var(--ff);
  max-width: 1300px;
  padding: 2rem;
  margin-inline: auto;
}

.title {
  text-align: center;
  font-size: 3rem;
  font-weight: 800;
  color: var(--clr-secondary);
  margin-block-end: 3rem;
}

.cards-layout {
  list-style: none;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(275px, 1fr));
  gap: 2rem;
}

.card-item {
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;

  &__title {
    font-weight: 800;
    color: var(--clr-secondary);
  }

  &__text-content {
    font-size: 0.825rem;
    font-weight: 500;
    color: var(--clr-primary);
  }

  &__content-container {
    padding: 1rem;
    display: flex;
    flex-flow: column nowrap;
    gap: 1rem;
  }

  &__image-text {
    font-weight: 700;
    font-size: 0.75rem;
    color: var(--clr-primary);
    opacity: 0.5;
  }
}

.card-footer {
  padding-block-start: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;

  &__creator {
    display: flex;
    gap: 0.5rem;
    align-items: center;
    font-size: 0.75rem;
    color: var(--clr-primary);
  }

  &__avatar {
    width: 2.25rem;
    height: 2.25rem;
    border-radius: 50%;
    object-fit: cover;
    object-position: center;
  }

  &__name {
    font-weight: 800;
  }

  &__date {
    opacity: 0.5;
  }

  &__btn {
    height: 1rem;
  }
}

// @media (min-width: 768px) {
// }
</style>
