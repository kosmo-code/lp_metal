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
                        <div class="products-armatures__item__title">{{ item.title }}</div>
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
                title: 'Арматура металлическая',
                to: '/products/armatures/'
            },
            {
                id: 2,
                img: "https://via.placeholder.com/150",
                title: 'Арматура композитная',
                to: '/products/armatures'
            },
            {
                id: 3,
                img: "https://via.placeholder.com/150",
                title: 'Арматура стеклопластиковая',
                to: '/products/armatures'
            },
            {
                id: 4,
                img: "https://via.placeholder.com/150",
                title: 'Арматура базальтопластиковая',
                to: '/products/armatures'
            },
            {
                id: 5,
                img: "https://via.placeholder.com/150",
                title: 'Арматура 6 мм',
                to: '/products/armatures'
            },
            {
                id: 6,
                img: "https://via.placeholder.com/150",
                title: 'Арматура 8 мм',
                to: '/products/armatures'
            },
            {
                id: 7,
                img: "https://via.placeholder.com/150",
                title: 'Арматура 10 мм',
                to: '/products/armatures'
            },
            {
                id: 8,
                img: "https://via.placeholder.com/150",
                title: 'Арматура 12 мм',
                to: '/products/armatures'
            },
            {
                id: 9,
                img: "https://via.placeholder.com/150",
                title: 'Арматура 14 мм',
                to: '/products/armatures'
            },
            {
                id: 10,
                img: "https://via.placeholder.com/150",
                title: 'Арматура 16 мм',
                to: '/products/armatures'
            },
            {
                id: 11,
                img: "https://via.placeholder.com/150",
                title: 'Арматура 20 мм',
                to: '/products/armatures'
            },
            {
                id: 12,
                img: "https://via.placeholder.com/150",
                title: 'Арматура А240 (АI, А1)',
                to: '/products/armatures'
            },
            {
                id: 13,
                img: "https://via.placeholder.com/150",
                title: 'Арматура А400 (АIII, А3)',
                to: '/products/armatures'
            },
            {
                id: 14,
                img: "https://via.placeholder.com/150",
                title: 'Арматура А500С',
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
.products-armatures {
    padding-top: 6rem;
}
.products-armatures__title {
    font-weight: 700;
    font-size: 2.5rem;
    line-height: 1.25;
    letter-spacing: 1.25px;
    margin-bottom: 2.5rem;
}
.products-armatures__list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    width: 100%;
    gap: .1rem .25rem;
    position: relative;
    margin-top: 2rem;
}
.products-armatures__item {
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 2rem 1.5rem 3rem;
    width: 250px;
    height: 13rem;
    margin: 1rem 0;
    display: inline-block;
    text-align: center;
    background-position: 100% 100%;
}
.products-armatures__item:first-child {
    margin-left: 0;
}
.products-armatures__item:last-child {
    margin-right: 0;
}
.products-armatures__item__img {
    width: 8rem;
    height: 8rem;
    border-radius: 5px;
    margin-bottom: 10px;
    object-fit: cover;
}
.products-armatures__item__title {
    font-size: 1.2rem;
    font-weight: 500;
    margin: .5rem 0 1.5rem;
}
.products-armatures__link {
    background-color: red;
    color: white;
    border: none;
    padding: .5rem 1rem;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    align-items: self-start;
    font-size: 1rem;
    border-radius: 5px;
    cursor: pointer;
}

</style>
