<template>
    <div>
        <section class="products-all">
            <div class="wrapper">
                <div class="products-all__title">Весь каталог</div>
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
                    <!--
                    <div class="category__wrapper">
                        <img class="arrow arrow__left" src="/left-arrow.svg" alt="Left arrow">
                        <ul class="carousel">
                            <li
                                class="card"
                                v-for="(card, index) in cards"
                                :key="index"
                            >
                                <img :src="card.img" alt="Product Image">
                                <h2>{{ card.title }}</h2>
                                <NuxtLink to="" class="btn__cta">Подробнее</NuxtLink>
                            </li>
                        </ul>
                        <img class="arrow arrow__right" src="/right-arrow.svg" alt="Right arrow">
                    </div> -->
                    <!-- Металлопрокат -->
                    <div class="category__wrapper">
                        <ul class="category-list">
                            <li
                                class="card"
                                v-for="(roledMetalItem, idx) in rolledMetalList"
                            >
                                <img :src="roledMetalItem.img" :alt="roledMetalItem.title">
                                <h2>{{ roledMetalItem.title }}</h2>
                                <NuxtLink :to="roledMetalItem.to" class="btn__cta">Подробнее</NuxtLink>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Труба -->
                <div class="inner__wrapper">
                    <h2 class="category__title">Каталог "Труба"</h2>
                    <div class="category__wrapper">
                        <ul class="category-list">
                            <li
                                class="card"
                                v-for="(tubeItem, idx) in tubeList"
                            >
                                <img :src="tubeItem.img" :alt="tubeItem.title">
                                <h2>Труба {{ tubeItem.title }}</h2>
                                <NuxtLink :to="tubeItem.to" class="btn__cta">Подробнее</NuxtLink>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Лист -->
                <div class="inner__wrapper">
                    <h2 class="category__title">Каталог "Лист"</h2>
                    <div class="category__wrapper">
                        <ul class="category-list">
                            <li
                                class="card"
                                v-for="(sheetMetalItem, idx) in sheetMetalList"
                            >
                                <img :src="sheetMetalItem.img" :alt="sheetMetalItem.title">
                                <h2>Лист {{ sheetMetalItem.title }}</h2>
                                <NuxtLink to="" class="btn__cta">Подробнее</NuxtLink>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Сетка -->
                <div class="inner__wrapper">
                    <h2 class="category__title">Каталог "Сетка"</h2>
                    <div class="category__wrapper">
                        <ul class="category-list">
                            <li
                                class="card"
                                v-for="(gridItem, idx) in gridList"
                            >
                                <img :src="gridItem.img" :alt="gridItem.title">
                                <h2>Лист {{ gridItem.title }}</h2>
                                <NuxtLink to="" class="btn__cta">Подробнее</NuxtLink>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Еще -->
                <div class="inner__wrapper">
                    <h2 class="category__title">Каталог "Еще"</h2>
                    <div class="category__wrapper">
                        <ul class="category-list">
                            <li
                                class="card"
                                v-for="(moreItem, idx) in moreList"
                            >
                                <img :src="moreItem.img" :alt="moreItem.title">
                                <h2>{{ moreItem.title }}</h2>
                                <NuxtLink to="" class="btn__cta">Подробнее</NuxtLink>
                            </li>
                        </ul>
                    </div>
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

        const rolledMetalList = ref([
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'Арматура',
                to: '/products/armatures'
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'Круг',
                to: '/products/circle',
            },
            {
                id: 3,
                img: "https://via.placeholder.com/150",
                title: 'Пруток',
                to: '/products/rod',
            },
            {
                id: 4,
                img: "https://via.placeholder.com/150",
                title: 'Балка двутавровая',
                to: '/products/I-beam',
            },
            {
                id: 5,
                img: "https://via.placeholder.com/150",
                title: 'Катанка',
                to: '/products/wire-rod',
            },
            {
                id: 6,
                img: "https://via.placeholder.com/150",
                title: 'Квадрат',
                to: '/products/square',
            },
            {
                id: 7,
                img: "https://via.placeholder.com/150",
                title: 'Лента',
                to: '/products/ribbon',
            },
            {
                id: 8,
                img: "https://via.placeholder.com/150",
                title: 'Лист',
                to: '/products/ribbon',
            },
            {
                id: 9,
                img: "https://via.placeholder.com/150",
                title: 'Поковка',
                to: '/products/ribbon',
            },
            {
                id: 10,
                img: "https://via.placeholder.com/150",
                title: 'Полоса',
                to: '/products/ribbon',
            },
            {
                id: 11,
                img: "https://via.placeholder.com/150",
                title: 'Проволока',
                to: '/products/ribbon',
            },
            {
                id: 12,
                img: "https://via.placeholder.com/150",
                title: 'Рельс',
                to: '/products/ribbon',
            },
            {
                id: 13,
                img: "https://via.placeholder.com/150",
                title: 'Сетка',
                to: '/products/ribbon',
            },
            {
                id: 14,
                img: "https://via.placeholder.com/150",
                title: 'Труба',
                to: '/products/ribbon',
            },
            {
                id: 15,
                img: "https://via.placeholder.com/150",
                title: 'Уголок металлический',
                to: '/products/ribbon',
            },
            {
                id: 16,
                img: "https://via.placeholder.com/150",
                title: 'Швеллер металлический',
                to: '/products/ribbon',
            },
            {
                id: 17,
                img: "https://via.placeholder.com/150",
                title: 'Штрипс',
                to: '/products/ribbon',
            },
            {
                id: 18,
                img: "https://via.placeholder.com/150",
                title: 'Шестигранник',
                to: '/products/ribbon',
            },
        ]);

        const tubeList = ref([
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'круглая',
                to: '/products/truba/kruglaya',
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'профильная',
                to: '/products/truba/profilnaya',
            },
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'квадратная',
                to: '/products/truba/square',
            },
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'прямоугольная',
                to: '/products/truba/rectangle',
            },
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'гофрированная',
                to: '/products/truba/gofrirovannaya',
            },
        ]);

        const tubeList2 = ref([
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'алюминиевая',
                to: '/products/truba/aluminiy',
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'асбестоцементная',
            },
            {
                id: 3,
                img: "https://via.placeholder.com/150",
                title: 'бронзовая',
            },
            {
                id: 4,
                img: "https://via.placeholder.com/150",
                title: 'бурильная',
            },
            {
                id: 5,
                img: "https://via.placeholder.com/150",
                title: 'в изоляции',
            },
            {
                id: 6,
                img: "https://via.placeholder.com/150",
                title: 'газлифтная',
            },
            {
                id: 7,
                img: "https://via.placeholder.com/150",
                title: 'дюралевая',
            },
            {
                id: 8,
                img: "https://via.placeholder.com/150",
                title: 'канализационная',
            },
            {
                id: 9,
                img: "https://via.placeholder.com/150",
                title: 'котельная',
            },
            {
                id: 10,
                img: "https://via.placeholder.com/150",
                title: 'крекинговая',
            },
            {
                id: 11,
                img: "https://via.placeholder.com/150",
                title: 'магистральная',
            },
            {
                id: 12,
                img: "https://via.placeholder.com/150",
                title: 'латунная',
            },
            {
                id: 13,
                img: "https://via.placeholder.com/150",
                title: 'нержавеющая круглая',
            },
            {
                id: 14,
                img: "https://via.placeholder.com/150",
                title: 'насосно-компрессорная (НКТ)',
            },
            {
                id: 15,
                img: "https://via.placeholder.com/150",
                title: 'медно-никелевая',
            },
            {
                id: 16,
                img: "https://via.placeholder.com/150",
                title: 'медная',
            },
            {
                id: 17,
                img: "https://via.placeholder.com/150",
                title: 'оцинкованная',
            },
            {
                id: 18,
                img: "https://via.placeholder.com/150",
                title: 'нержавеющая электросварная',
            },
            {
                id: 19,
                img: "https://via.placeholder.com/150",
                title: 'обсадная',
            },
            {
                id: 20,
                img: "https://via.placeholder.com/150",
                title: 'НПВХ',
            },
            {
                id: 21,
                img: "https://via.placeholder.com/150",
                title: 'ПВХ',
            },
            {
                id: 22,
                img: "https://via.placeholder.com/150",
                title: 'полипропиленовая',
            },
            {
                id: 23,
                img: "https://via.placeholder.com/150",
                title: 'полиэтиленовая ПЭ',
            },
            {
                id: 24,
                img: "https://via.placeholder.com/150",
                title: 'прецизионная',
            },
            {
                id: 25,
                img: "https://via.placeholder.com/150",
                title: 'бесшовная',
            },
            {
                id: 26,
                img: "https://via.placeholder.com/150",
                title: 'стальная квадратная',
            },
            {
                id: 27,
                img: "https://via.placeholder.com/150",
                title: 'водогазопроводная (ВГП)',
            },
            {
                id: 28,
                img: "https://via.placeholder.com/150",
                title: 'горячедеформированная',
            },
            {
                id: 29,
                img: "https://via.placeholder.com/150",
                title: 'электросварная',
            },
            {
                id: 30,
                img: "https://via.placeholder.com/150",
                title: 'холоднодеформированная',
            },
            {
                id: 31,
                img: "https://via.placeholder.com/150",
                title: 'стальная прямоугольная',
            },
            {
                id: 32,
                img: "https://via.placeholder.com/150",
                title: 'стальная профильная',
            },
            {
                id: 33,
                img: "https://via.placeholder.com/150",
                title: 'титановая',
            },
            {
                id: 34,
                img: "https://via.placeholder.com/150",
                title: 'чугунная',
            },
        ]);

        const sheetMetalList = ref([
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'гладкий ',
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'рифленый',
            },
            {
                id: 3,
                img: "https://via.placeholder.com/150",
                title: 'перфорированный',
            },
            {
                id: 4,
                img: "https://via.placeholder.com/150",
                title: 'просечно-вытяжной ПВЛ',
            },
            {
                id: 5,
                img: "https://via.placeholder.com/150",
                title: 'Катанка',
            },
        ]);

        const gridList = ref([
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'рабица ',
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'сварная',
            },
            {
                id: 3,
                img: "https://via.placeholder.com/150",
                title: 'тканая',
            },
        ]);

        const moreList = ref([
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'Проволока',
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'Трубопроводная арматура',
            },
            {
                id: 3,
                img: "https://via.placeholder.com/150",
                title: 'АТИ',
            },
            {
                id: 4,
                img: "https://via.placeholder.com/150",
                title: 'Композит',
            },
            {
                id: 5,
                img: "https://via.placeholder.com/150",
                title: 'Катанка',
            },
            {
                id: 6,
                img: "https://via.placeholder.com/150",
                title: 'Профиль алюминиевый',
            },
            {
                id: 7,
                img: "https://via.placeholder.com/150",
                title: 'Воздуховод',
            },
            {
                id: 8,
                img: "https://via.placeholder.com/150",
                title: 'Дымоход',
            },
            {
                id: 9,
                img: "https://via.placeholder.com/150",
                title: 'Кровельные материалы',
            },
            {
                id: 10,
                img: "https://via.placeholder.com/150",
                title: 'РТИ',
            },
            {
                id: 11,
                img: "https://via.placeholder.com/150",
                title: 'Отопительные приборы',
            },
            {
                id: 12,
                img: "https://via.placeholder.com/150",
                title: 'Сплавы',
            },
            {
                id: 13,
                img: "https://via.placeholder.com/150",
                title: 'Сетка',
            },
            {
                id: 14,
                img: "https://via.placeholder.com/150",
                title: 'Труба',
            },
            {
                id: 15,
                img: "https://via.placeholder.com/150",
                title: 'Уголок металлический',
            },
            {
                id: 16,
                img: "https://via.placeholder.com/150",
                title: 'Швеллер металлический',
            },
            {
                id: 17,
                img: "https://via.placeholder.com/150",
                title: 'Штрипс',
            },
            {
                id: 18,
                img: "https://via.placeholder.com/150",
                title: 'Шестигранник',
            },
        ]);

        return {
            searchLoading,
            toggleSearchLoading,
            rolledMetalList,
            tubeList,
            sheetMetalList,
            gridList,
            moreList,
        };
    },
}
</script>

<style scoped lang="scss">
@import "assets/styles/index";

.arrow {
    top: 50%;
    transform: translateY(-50%);
    width: 1rem;
    height: 1rem;
    border: 1px solid #cccccc;
    border-radius: 50px;
    padding: .5rem;
    cursor: pointer;
    position: absolute;
    box-shadow: 0 3px 6px rgba(0, 0, 0, .23);
    &:hover,
    &:focus {
        background-color: #cccccc;
        transition: background-color .75s;
    }
    &__left {
        left: -22px;
    }
    &__right {
        right: -22px;
    }
}
.carousel {
    display: grid;
    grid-auto-flow: column;
    grid-auto-columns: calc((100% / 4) - .75rem);
    gap: 1rem;
    overflow: hidden;
}
</style>
