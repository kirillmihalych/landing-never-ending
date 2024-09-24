<template>
  <div class="feature-list-layout-container">
    <h2 class="title">Ведьмачьи ROA <span>в .png</span></h2>
    <ul class="feature-list-layout">
      <li class="feature-item">
        <img src="../assets/images/коа_арт_пнг/аедирн_ком.png" alt="нильфгаард_ком" class="feature-item__png" />
        <h3>Аедирн!</h3>
        <p>
          Одно из крупнейших и могущественных королевств Севера, расположенное у склонов Синих гор к югу от Понтара и
          известное своим сельским хозяйством и развитой промышленностью.
        </p>
      </li>
      <li class="feature-item">
        <img src="../assets/images/коа_арт_пнг/редания_ком.png" alt="редания_ком" class="feature-item__png" />
        <h3>Редания!</h3>
        <p>
          Одно из самых крупных и могущественных королевств Севера, расположенное между реками Браа и Понтар и известное
          своей мощной экономикой, развитым сельским хозяйством и дворянством.
        </p>
      </li>
      <li class="feature-item">
        <img src="../assets/images/коа_арт_пнг/каедвен_ком.png" alt="каедвен_ком" class="feature-item__png" />
        <h3>Каедвен!</h3>
        <p>
          Одно из крупнейших и могущественных королевств Севера, известное своим суровым, холодным климатом, а также
          обширными хвойными лесами.
        </p>
      </li>
      <li class="feature-item">
        <img src="../assets/images/коа_арт_пнг/темерия_ком.png" alt="темерия_ком" class="feature-item__png" />
        <h3>Темерия!</h3>
        <p>
          Одно из самых крупных и могущественных королевств Севера, имеющее важное как стратегическое, так и
          политическое значение.
        </p>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

@font-face {
  font-family: witcher;
  src: url(../assets/fonts/masonchronicles.ttf);
}

.feature-list-layout-container {
  --font-heading: witcher;
  --font-text: 'Roboto', system-ui;
  --clr-text: #7e7e7e;

  max-width: 1300px;
  padding: 1rem;
  margin-inline: auto;
  font-family: var(--font-text);
}

.title {
  font-family: var(--font-heading);
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;

  span {
    display: block;
    font-size: 1.5rem;
    color: var(--clr-text);
    font-weight: 100;
  }
}

.feature-list-layout {
  list-style: none;
}

.feature-list-layout {
  margin-block-start: 4rem;
  display: grid;
  justify-content: center;
  gap: 1.25rem;
}

.feature-item {
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
  padding: 1rem;
  // shadows

  &__png {
    max-width: 7rem;
    max-height: 7rem;
    object-fit: contain;
    // filter: drop-shadow(0px 0px 10px rgba(0 0 0 / 30%));
    filter: drop-shadow(2px 2px 5px hsl(22, 100%, 50%));
  }

  h3 {
    font-weight: 700;
    font-size: 1.25rem;
    font-family: var(--font-heading);
    margin-block-end: 0.5rem;
    font-weight: 700;
  }

  p {
    color: var(--clr-text);
    line-height: 1.25rem;
    text-align: center;
    font-size: 0.75rem;
  }
}

@media (min-width: 480px) {
  .feature-list-layout {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }
}
</style>
