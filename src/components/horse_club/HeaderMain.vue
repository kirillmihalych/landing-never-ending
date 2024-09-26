<template>
  <div class="main-container">
    <div class="layout-container">
      <header class="header">
        <img src="../../assets/images/background/horse_club/logo_horse_club.png" alt="logo" class="header__logo" />
        <div class="header__right-part-container">
          <nav class="header__nav">
            <a href="#" class="link-active-underline"> О нас </a>
            <a href="#"> Услуги и цены </a>
            <a href="#"> Фотоальбом </a>
            <a href="#"> Контакты </a>
          </nav>
          <aside class="header__aside">
            <img src="../../assets/images/background/horse_club/phone_svg.svg" alt="phone_svg" />
            <p class="header__aside--phone-number">+7 (000) 000-00-00</p>
          </aside>
        </div>
        <button class="header__burger-menu-btn">
          <img src="../../assets/images/background/horse_club/burger-bar.png" alt="burgen icon btn" />
          <span>Меню</span>
        </button>
      </header>
      <section class="promo-container">
        <h1 class="promo-container__title">
          Окунитесь в мир <br />
          лошадей вместе с нами
        </h1>
        <div class="promo-container__text">
          <p>
            Уроки верховой езды, фотосессии и мероприятия <br />
            в частном конном клубе<span class="promo-container__text--city"> г. Санкт-Петербург</span>
          </p>
        </div>
        <button class="promo-container__btn">Записаться</button>
      </section>
    </div>
  </div>
</template>

<style lang="scss" scoped>
// utils
.link-active-underline {
  border-block-end: 1px solid green;
}

// layout
.layout-container {
  max-width: 1000px;
  margin-inline: auto;
}

.main-container {
  font-family: 'Roboto', system-ui;
  background-repeat: no-repeat;
  background-size: contain;
  background-position: top center;
  background-attachment: fixed;
  object-fit: cover;
  height: 100vh;

  @media (max-width: 480px) {
    background-image: url('../../assets/images/background/horse_club/bg-320.png');
  }

  @media (min-width: 480px) {
    background-size: cover;
    background-image: url('../../assets/images/background/horse_club/bg-480.png');
  }

  @media (min-width: 768px) {
    background-image: url('../../assets/images/background/horse_club/bg-768.png');
  }

  @media (min-width: 1000px) {
    background-size: cover;
    background-image: url('../../assets/images/background/horse_club/bg-1000.jpg');
  }
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 60px;
  padding: 1rem;

  &__logo {
    height: 2rem;

    @media (min-width: 768px) {
      height: 2.5rem;
    }

    @media (min-width: 1000px) {
      height: 3rem;
    }
  }

  &__burger-menu-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0.5rem;
    gap: 0.25rem;
    background: transparent;
    border: 1px solid var(--clr-green);
    border-radius: 0.25rem;
    line-height: 1rem;

    img {
      height: 0.75rem;
    }

    &:hover {
      cursor: pointer;
    }

    @media (min-width: 768px) {
      display: none;
    }
  }

  &__nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1.5rem;

    a {
      text-decoration: none;
      text-transform: uppercase;
      color: #202020;
      font-size: 0.75rem;
      padding-block: 0.625rem;

      @media (min-width: 1000px) {
        font-size: 0.825rem;
      }
    }
  }

  &__right-part-container {
    display: none;
    gap: 3.5rem;

    @media (min-width: 768px) {
      display: flex;
    }
  }

  &__aside {
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  &__aside--phone-number {
    display: flex;
    align-items: center;
    font-weight: 700;
    font-size: 0.75rem;
    position: relative;

    @media (min-width: 1000px) {
      font-size: 1.125rem;
    }
  }

  &__aside--phone-number::after {
    content: 'Ежедневно 9:00 – 22:00';
    display: block;
    position: absolute;
    top: 0;
    margin-block-start: 1.25rem;
    color: #7d808a;
    font-weight: 400;
    font-size: 0.5rem;

    @media (min-width: 1000px) {
      margin-block-start: 1.75rem;
      font-size: 0.75rem;
    }
  }
}

.promo-container {
  width: calc(100% - 2rem);
  margin-inline: auto;
  margin-block-start: 5.5rem;
  display: grid;
  justify-items: center;

  @media (min-width: 768px) {
    justify-items: start;
  }

  @media (min-width: 1000px) {
    margin-block-start: 3rem;
  }

  &__title {
    font-family: 'Philosopher', sans-serif;
    font-size: 1.5rem;
    font-weight: 700;
    text-align: center;

    @media (min-width: 480px) {
      font-size: 2.5rem;
    }

    @media (min-width: 768px) {
      text-align: start;
      font-size: 2.5rem;
    }

    @media (min-width: 1000px) {
      font-size: 3rem;
    }
  }

  &__text {
    margin-block-start: 2.5rem;
    font-family: 'Alegreya Sans', sans-serif;
    font-size: 0.75rem;
    line-height: 1rem;
    color: #646464;
    text-align: center;
    &--city {
      font-weight: 700;
    }

    @media (min-width: 480px) {
      line-height: 1.5rem;
      font-size: 1rem;
    }

    @media (min-width: 768px) {
      text-align: start;
      font-size: 1.25rem;
    }

    @media (min-width: 1000px) {
      font-size: 1.25rem;
      line-height: 1.4;
      margin-block-start: 1.5rem;
    }
  }

  &__btn {
    font-family: 'Montserrat', system-ui;
    font-size: 0.5rem;
    font-weight: 600;
    line-height: 0.5rem;
    letter-spacing: 0.07rem;
    color: #6a5300;
    border: none;
    margin-block-start: 2.75rem;
    text-transform: uppercase;
    box-shadow: 0px 3px 0px #6a5300;
    background: linear-gradient(#fff383 25%, #ffc700);
    border-radius: 0.25rem;
    padding-inline: 3rem;
    padding-block: 1rem;

    @media (min-width: 480px) {
      font-size: 0.625rem;
    }

    @media (min-width: 768px) {
      line-height: 2rem;
      padding-block: 0.5rem;
      justify-self: start;
    }

    @media (min-width: 1000px) {
      padding-block: 1rem;
      padding-inline: 3.5rem;
      font-size: 0.75rem;
    }
  }

  &__btn:hover {
    cursor: pointer;
    background: linear-gradient(#fff383 5%, #ffc700);
  }

  &__btn:active {
    background: linear-gradient(#ffc700 95%, #fff383);
  }
}
</style>
