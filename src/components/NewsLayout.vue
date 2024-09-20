<template>
  <section class="news">
    <h2 class="title">Новости</h2>
    <ul class="news-layout">
      <li v-for="news_item in news" :key="news_item.id" class="item">
        <img src="../assets/images/скрины_жпеги/жпег_скрин_10.jpg" :alt="news_item.alt" class="item__img" />
        <div class="item-content">
          <p class="item-content__alt">{{ news_item.alt }}</p>
          <h3 class="item-content__title">{{ news_item.title }}</h3>
          <p class="item-content__text">{{ news_item.content }}</p>
          <footer class="card-footer">
            <div>
              <img src="../assets/images/коа_арт_пнг/аедирн_ком.png" :alt="news_item.author" class="avatar" />
              <div>
                <p>{{ news_item.author }}</p>
                <p>{{ news_item.date }}</p>
              </div>
            </div>
            <a href="#">
              <img src="../assets/images/icons/share_icon.png" alt="share-icon" />
            </a>
          </footer>
        </div>
      </li>
    </ul>
  </section>
</template>

<script setup lang="ts">
const news = [
  {
    id: 1,
    alt: 'Геральт на переговорах стоит',
    title: 'Сказанное Геральто повергло в шок',
    content:
      'Быть нейтральным — не значит быть равнодушным и бесчувственным. Не надо убивать в себе чувства. Достаточно убить в себе ненависть.',
    author: 'Денис Аердинский',
    date: Date.now(),
  },
  {
    id: 2,
    alt: 'Геральт на переговорах стоит',
    title: 'Сказанное Геральто повергло в шок',
    content:
      'Быть нейтральным — не значит быть равнодушным и бесчувственным. Не надо убивать в себе чувства. Достаточно убить в себе ненависть.',
    author: 'Денис Аердинский',
    date: Date.now(),
  },
  {
    id: 3,
    alt: 'Геральт на переговорах стоит',
    title: 'Сказанное Геральто повергло в шок',
    content:
      'Быть нейтральным — не значит быть равнодушным и бесчувственным. Не надо убивать в себе чувства. Достаточно убить в себе ненависть.',
    author: 'Денис Аердинский',
    date: Date.now(),
  },
]
</script>

<style scoped lang="scss">
.news {
  padding: 1rem;
}

.title {
  text-align: center;
  margin-block: 3rem;
  font-size: 3rem;
  font-weight: 700;
  color: #163152;
}

.news-layout {
  display: grid;
  gap: 2rem;
  list-style: none;
}

.item {
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}

.item-content {
  padding: 1.25rem;
  padding-block-start: 0;

  &__alt {
    color: #283c54;
    opacity: 0.5;
    font-weight: 700;
    font-size: 0.85rem;
    margin-block-start: 0.625rem;
  }

  &__title {
    margin-block-start: 0.75rem;
    color: #163152;
    font-weight: 800;
    font-size: 1rem;
  }

  &__text {
    margin-block-start: 0.5rem;
    font-size: 0.875rem;
    color: #283c54;
  }
}

.card-footer {
  margin-block-start: 1.25rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.75rem;

  div:first-child {
    display: flex;
    align-items: center;
    gap: 1rem;
    font-weight: 700;
    color: #283c54;

    p:last-child {
      margin-block-start: 0.5rem;
      opacity: 0.5;
    }
  }
}

.avatar {
  width: 4rem;
  height: 4rem;
  border-radius: 50%;
}

@media (min-width: 1200px) {
  .news {
    padding: 100px;
  }

  .avatar {
    width: 2rem;
    height: 2rem;
    border-radius: 50%;
  }

  .news-layout {
    grid-template-columns: repeat(3, minmax(0, 1fr));
    grid-auto-rows: 330px;
  }

  .item__img {
    width: 100%;
  }

  .item:first-child {
    grid-column: 1 / 3;
    grid-row: 1 / 3;

    .item__img {
      height: 55%;
      object-fit: cover;
      object-position: top center;
    }

    .item-content {
      padding: 2.5rem;
      padding-block-start: 0;

      &__title {
        margin-block-start: 1.25rem;
        font-size: 1.375rem;
      }

      &__text {
        margin-block-start: 0.85rem;
        font-size: 1.125rem;
      }
    }

    .card-footer {
      margin-block-start: 2rem;
      font-size: 1rem;

      .avatar {
        width: 4rem;
        height: 4rem;
      }
    }
  }

  .item:nth-child(2) {
    grid-column: 3 / 4;
    .item__img {
      height: 40%;
      width: 100%;
      object-fit: cover;
      object-position: top center;
    }
  }

  .item:last-child {
    grid-column: 3 / 4;
    .item__img {
      height: 40%;
      width: 100%;
      object-fit: cover;
      object-position: top center;
    }
  }
}
</style>
