<template>
    <div>
        <section class="products-armatures">
            <div class="wrapper">
                <h3 class="products-armatures__title">Труба круглая</h3>
                <div id="search" :class="{ 'search__loading': searchLoading }">
                    <input class="search__input" type="text" id="input" placeholder="Поиск..." @keyup.enter="toggleSearchLoading" />
                    <button class="search__btn" id="button" @click="toggleSearchLoading">
                        <img src="/search.svg" alt="Search svg-icon">
                    </button>
                    <div class="search__spinner">
                        <img src="/loader.svg" alt="Loader svg-icon">
                    </div>
                </div>
                <ul class="products-armatures__list">
                    <li
                      class="products-armatures__item"
                      v-for="(item, idx) in trubaList"
                      :key="idx"
                    >
                        <img :src="item.img" :alt="item.title" class="products-armatures__item__img">
                        <div class="products-armatures__item__title">Труба круглая <br>{{ item.title }}</div>
                        <!-- modal-popup -->
                        <NuxtLink class="products-armatures__link">Посмотреть</NuxtLink>
                    </li>
                </ul>
            </div>
        </section>
        <!-- /.products-armatures -->
    </div>
</template>

<script>
export default {
    name: "kruglaya",
    setup() {
        const trubaList = ref([
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
                title: 'насосно-компрессорная',
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

        return {
            trubaList,
        };
    },
}
</script>

<style scoped lang="scss">
@import "assets/styles/index";
</style>
