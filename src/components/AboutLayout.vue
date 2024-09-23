<template>
  <div class="about-layout-container">
    <h2 class="title">О нашем клубе</h2>
    <div class="about-layout">
      <div class="about-grid">
        <img src="../assets/images/скрины_жпеги/жпег_скрин_1.jpg" alt="жпег_скрин_1" class="img-floated" />
        <ul class="about-subgrid">
          <li>
            <p>1000+</p>
            <p>Довольный посетителей за последний год</p>
          </li>
          <li>
            <p>50+</p>
            <p>Проведенных мероприятий за 6 месяцев</p>
          </li>
          <li>
            <p>20+</p>
            <p>Выпущенных профессиональных спортсменов за 1 год</p>
          </li>
          <li>
            <p>15+</p>
            <p>Регулярный занятий в неделю с профессиональными наставниками</p>
          </li>
        </ul>
      </div>
      <p class="text-content">
        Занятия проводятся индивидуально и в группах, стоимость также будет зависеть от ваших навыков и умений. Более
        выгодные условия предусмотрены для регулярных занятий при покупке абонементов. Для тех, кто хочет отточить своё
        мастерство, разработаны программы по специализации (конкур, выездка и другие), участие в соревнованиях
        и чемпионатах. Для самых маленьких любителей лошадей действуют пони-клубы, где ребята учатся ухаживать
        за животными и ездить на милых и добрых пони.
      </p>
    </div>
    <ul></ul>
  </div>
</template>

<script></script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Philosopher:wght@400;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,500;1,300&display=swap');

.about-layout-container {
  --font-heading: 'Philosopher', sans-serif;
  --font-text: 'Roboto', sans-serif;
  --clr-heading: #0b0b0b;
  --clr-subheading: #008139;
  --clr-text: #7e7e7e;

  max-width: 1300px;
  font-family: var(--font-text);
  padding: 1rem;
  margin-inline: auto;
}

.img-floated {
  border-radius: 1.5rem;
  display: none;
}

.title {
  text-align: center;
  color: var(--clr-heading);
  font-family: var(--font-heading);
  font-size: 2.5rem;
  line-height: 2.25rem;
  margin-block-end: 2.5rem;
}

.about-grid {
  display: grid;
  gap: 2rem;
}

.about-subgrid {
  list-style: none;
  display: grid;
  gap: 2rem;
  justify-items: center;

  li {
    align-self: start;
    text-align: center;
  }

  li > p:first-child {
    font-family: var(--font-heading);
    font-size: 2rem;
    font-weight: 700;
    line-height: 1.6;
    color: var(--clr-subheading);
  }

  li > p:last-child {
    font-family: var(--font-text);
    font-size: 1rem;
    color: var(--clr-heading);
    line-height: 1.5rem;
    font-weight: 500;
  }
}

.text-content {
  margin-block-start: 2rem;
  color: var(--clr-text);
  line-height: 1.25rem;
  font-size: 0.825rem;
}

@media (min-width: 480px) {
  .about-subgrid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 768px) {
  .about-grid {
    grid-template-columns: 1fr 1fr;
  }

  .img-floated {
    display: block;
    height: 100%;
    object-fit: cover;
    object-position: center;
  }
}
</style>
