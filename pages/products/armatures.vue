<template>
    <div>
        <section class="products-armatures">
            <div class="wrapper">
                <h3 class="products-armatures__title">Арматура</h3>
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
                        v-for="(item, idx) in armaturesList"
                        :key="idx"
                    >
                        <img :src="item.img" :alt="item.title" class="products-armatures__item__img">
                        <div class="products-armatures__item__title">Арматура {{ item.title }}</div>
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
import Default from "~/layouts/default.vue";

export default {
    name: "armatures",
    components: {Default},
    setup() {
        const armaturesList = ref([
            {
                id: 1,
                img: "https://via.placeholder.com/150",
                title: 'металлическая',
                to: '/products/armatures/'
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'композитная',
                to: '/products/armatures'
            },
            {
                id: 3,
                img: "https://via.placeholder.com/150",
                title: 'стеклопластиковая',
                to: '/products/armatures'
            },
            {
                id: 4,
                img: "https://via.placeholder.com/150",
                title: 'базальтопластиковая',
                to: '/products/armatures'
            },
            {
                id: 5,
                img: "https://via.placeholder.com/150",
                title: '6 мм',
                to: '/products/armatures'
            },
            {
                id: 6,
                img: "https://via.placeholder.com/150",
                title: '8 мм',
                to: '/products/armatures'
            },
            {
                id: 7,
                img: "https://via.placeholder.com/150",
                title: '10 мм',
                to: '/products/armatures'
            },
            {
                id: 8,
                img: "https://via.placeholder.com/150",
                title: '12 мм',
                to: '/products/armatures'
            },
            {
                id: 9,
                img: "https://via.placeholder.com/150",
                title: '14 мм',
                to: '/products/armatures'
            },
            {
                id: 10,
                img: "https://via.placeholder.com/150",
                title: '16 мм',
                to: '/products/armatures'
            },
            {
                id: 11,
                img: "https://via.placeholder.com/150",
                title: '20 мм',
                to: '/products/armatures'
            },
            {
                id: 12,
                img: "https://via.placeholder.com/150",
                title: 'А240 (АI, А1)',
                to: '/products/armatures'
            },
            {
                id: 13,
                img: "https://via.placeholder.com/150",
                title: 'А400 (АIII, А3)',
                to: '/products/armatures'
            },
            {
                id: 14,
                img: "https://via.placeholder.com/150",
                title: 'А500С',
                to: '/products/armatures'
            },
        ]);

        return {
            armaturesList,
        };
    },
}
</script>

<style scoped lang="scss">
@import "assets/styles/index";
</style>
