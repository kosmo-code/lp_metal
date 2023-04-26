<template>
    <div>
        <section class="products-all">
            <div class="wrapper">
                <div>
                    <div>Каталог товаров</div>
                    <div id="search" :class="{ 'search__loading': searchLoading }">
                        <input class="search__input" type="text" id="input" placeholder="Поиск..." @keyup.enter="toggleSearchLoading" />
                        <button class="search__btn" id="button" @click="toggleSearchLoading">
                            <img src="/search.svg" alt="Search svg-icon">
                        </button>
                        <div class="search__spinner">
                            <img src="/loader.svg" alt="Loader svg-icon">
                        </div>
                    </div>
                    <div style="color: red">Фильтр по параметру</div>
                    <div class="inner__wrapper">
                        <h2 class="category__title">Каталог "Металлопрокат"</h2>
                        <div class="category__wrapper">
                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Арматура</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Круг</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Пруток</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Балка двутавровая</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Катанка</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Квадрат</h2>
                                <button>Подробнее</button>
                            </NuxtLink>



                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Лента</h2>
                                <button>Подробнее</button>
                            </NuxtLink>
                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Лист</h2>
                                <button>Подробнее</button>
                            </NuxtLink>
                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Поковка</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Поковка</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Полоса</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Проволока</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Рельс</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Сетка</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Сетка</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Труба</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Уголок металлический</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Уголок металлический</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Швеллер металлический</h2>
                                <button>Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Штрипс</h2>
                                <button class="btn__cta">Подробнее</button>
                            </NuxtLink>

                            <NuxtLink to="" class="card">
                                <img src="https://via.placeholder.com/150" alt="Product Image">
                                <h2>Шестигранник</h2>
                                <button class="btn__cta">Подробнее</button>
                            </NuxtLink>
                        </div>
                    </div>
<!--                    <div class="category__wrapper">-->
<!--                        <h2 class="category__title">Каталог "Металлопрокат"</h2>-->
<!--                        <div class="category__content">-->
<!--                            <div class="category__content">-->
<!--                                <NuxtLink to="/">-->
<!--                                    <img class="products-all__content__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="Photo of category">-->
<!--                                    <h3 class="products-all__content__card-title">Мателлопрокат</h3>-->
<!--                                    <button class="btn__cta">перейти</button>-->
<!--                                </NuxtLink>-->
<!--                            </div>-->
<!--                        </div>-->
<!--                    </div>-->
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import Default from "~/layouts/default.vue";

export default {
    name: "all",
    components: {Default},
    setup() {
        const searchLoading = ref(true);

        const toggleSearchLoading = () => {
            searchLoading.value = false;

            setTimeout(() => {
                searchLoading.value = true;
            }, 1500);

            searchLoading.value = false;
        };

        return {
            searchLoading,
            toggleSearchLoading,
        };
    },
}
</script>

<style scoped lang="scss">
@import "assets/styles/index";

.card {
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 2rem 0;
    width: 15rem;
    height: 100%;
    margin: 1rem;
    display: inline-block;
    text-align: center;
}

.card img {
    width: 40%;
    border-radius: 5px;
    margin-bottom: 10px;
}

.card h2 {
    font-size: 1.25rem;
    margin-bottom: 0.8rem;
}

.card button {
    background-color: red;
    color: white;
    border: none;
    padding: .8rem 1rem;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    align-items: self-start;
    font-size: 1rem;
    border-radius: 5px;
    cursor: pointer;
}






.products-all {
    padding: 6rem 1rem 1rem;
    margin: 2.5rem 0;
}

.inner__wrapper {
    min-height: 100vh;
    width: 100%;
    margin-top: 2.5rem;
}

.category__wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 1rem;
}

#search {
  align-items: center;;
  background: #F8F8F8;
  border-radius: 10px;
  display: flex;
  justify-content: space-between;
  margin: 0.5em 0;
  padding: 0.5em 0.5em 0.5em 1em;
  width: 500px;
  transition: all 0.5s;
  &__btn,
  &__input {
    appearance: none;
    background: transparent;
    border: 0;
    color: inherit;
    font: inherit;
    outline: 0;
  }
  &__btn {
    cursor: pointer;
    padding: 0 0.25em;
  }
  &__input {
    flex: 1;
    &::placeholder {
      color: black;
    }
  }
}
.search__spinner {
  animation: spinner 1s infinite linear;
  display: none;
  padding: 0 0.25em;
}

#search.loading {
  .search__btn {
    display: none;
  }
}
#search.loading {
  .search__spinner {
    display: block;
  }
}

// Animation

@keyframes search__spinner {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

</style>
