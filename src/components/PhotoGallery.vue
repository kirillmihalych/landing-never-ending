<template>
  <div class="container">
    <h2 class="container__title">Photo Gallery</h2>
    <div class="container__text">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      <p>Phasellus dapibus mauris in lectus tempus, eget tincidunt.</p>
    </div>
    <ul class="photo-gallery">
      <li>
        <img src="../assets/images/скрины_жпеги/жпег_скрин_1.jpg" alt="жпег_скрин_1.jpg" />
      </li>
      <li>
        <img src="../assets/images/скрины_жпеги/жпег_скрин_2.jpg" alt="жпег_скрин_2.jpg" />
      </li>
      <li>
        <img src="../assets/images/скрины_жпеги/жпег_скрин_3.jpg" alt="жпег_скрин_3.jpg" />
      </li>
      <li>
        <img src="../assets/images/скрины_жпеги/жпег_скрин_4.jpg" alt="жпег_скрин_4.jpg" />
      </li>
      <li>
        <img src="../assets/images/скрины_жпеги/жпег_скрин_5.jpg" alt="жпег_скрин_5.jpg" />
      </li>
      <li>
        <img src="../assets/images/скрины_жпеги/жпег_скрин_6.jpg" alt="жпег_скрин_6.jpg" />
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&display=swap');

.container {
  --color-dark-blue: #010a20;
  --color-light-grey: #6f7787;
  --fw-bold: 800;
  --fs-mid: 2.5rem;
  --fs-xxl: 3.75rem;

  font-family: 'DM Sans', sans-serif;
  width: min(100% - 2rem, 60rem);
  margin-inline: auto;

  display: grid;
  gap: 1.25rem;
  place-items: center;

  &__title {
    margin-block-start: 1.25rem;
    text-align: center;
    font-size: var(--fs-mid);
    font-weight: var(--fw-bold);
    color: var(--color-dark-blue);
  }

  &__text {
    text-align: center;
    color: var(--color-light-grey);
    line-height: 1.5rem;
    margin-block-end: 1.25rem;
  }
}

.photo-gallery {
  list-style: none;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(4, 1fr);
  grid-auto-rows: minmax(4.75rem, auto);
  gap: 0.75rem;
  margin-block-end: 2rem;
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.photo-gallery > li {
  border-radius: 0.625rem;
  overflow: hidden;
}

li:nth-child(1) {
  grid-column: span 2;
  grid-row: 1 / span 2;
}

li:nth-child(2) {
  grid-column: span 2;
}

li:nth-child(3) {
  grid-column: span 2;
  grid-row: 2 / span 2;
}

li:nth-child(4) {
  grid-column: span 2;
}

li:nth-child(5) {
  grid-column: span 2;
  grid-row: span 2;
}

li:nth-child(6) {
  grid-row: span 2;
  grid-column: span 2;
}

@media (min-width: 768px) {
  .photo-gallery {
    grid-template-columns: repeat(6, 1fr);
  }

  li:nth-child(1) {
    grid-column: span 2;
    grid-row: 1 / span 3;
  }

  li:nth-child(3) {
    grid-column: span 2;
    grid-row: 2 / span 3;
  }

  li:nth-child(5) {
    grid-row: 1 / span 2;
    grid-column: 5 / span 2;
  }

  li:nth-child(6) {
    grid-row: 3 / span 2;
    grid-column: 5 / span 2;
  }
}
</style>
