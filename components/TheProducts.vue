<template>
    <div class="products__wrapper">
        <div class="wrapper ">
            <section class="main__section">
                <div class="wrapper">
                    <div class="main__row">
                        <div class="main__row__banner">
                            <img src="https://images.unsplash.com/photo-1515630771457-09367d0ae038?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"
                                 alt="img of metal fabric">
                        </div>
                        <div class="main__card one">
                            <NuxtLink to="">
                                <img src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="" class="main__card-img">
                            </NuxtLink>
                            <NuxtLink to="">
                                <h3 class="main__card-title">Сортовый прокат</h3>
                            </NuxtLink>
                            <div class="main__card__bottom">
                                <button class="main__card__bottom-btn">+4 категории</button>
                                <span class="main__card__bottom-price">от 53.00 руб./м</span>
                            </div>
                        </div>
                        <div class="main__card two">
                            <NuxtLink to="">
                                <img src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="" class="main__card-img">
                            </NuxtLink>
                            <NuxtLink to="">
                                <h3 class="main__card-title">Арматура</h3>
                            </NuxtLink>
                            <div class="main__card__bottom">
                                <button class="main__card__bottom-btn">+4 категории</button>
                                <span class="main__card__bottom-price">от 53.00 руб./м</span>
                            </div>
                        </div>
                    </div>

                    <!-- First variant of catalog -->
                    <div class="main__row-2">
                        <NuxtLink to="" class="main__card third">
                            <h3 class="main__card-title">Сортовый прокат</h3>
                            <p class="main__card-description">Lorem ipsum dolor sit.</p>
                            <img class="main__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="">
                        </NuxtLink>
                        <NuxtLink to="" class="main__card fourth">
                            <h3 class="main__card-title">Сортовый прокат</h3>
                            <p class="main__card-description">Lorem ipsum dolor sit.</p>
                            <img class="main__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="">
                        </NuxtLink>
                        <NuxtLink to="" class="main__card fifth">
                            <h3 class="main__card-title">Сортовый прокат</h3>
                            <p class="main__card-description">Lorem ipsum dolor sit.</p>
                            <img class="main__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="">
                        </NuxtLink>
                    </div>

                    <div class="el-center">
                        <NuxtLink to="/products/all" class="btn__cta">Смотреть все разделы</NuxtLink>
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>

<script>
export default {
    name: "TheProducts",
}
</script>

<style scoped lang="css">
@import "assets/styles/index.css";

.el-center {
    display: flex;
    align-items: center;
    justify-content: center;
}

.products__wrapper {
    height: 100vh;
    margin: 4rem 0 -2rem;
}

.main__row {
    display: grid;
    grid-template-columns: 3fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-column-gap: 2.5rem;
    grid-row-gap: 2.5rem;
    grid-template-areas: "banner card" "banner card2";
    margin-bottom: 2.5rem;
}

.main__row__banner {
    grid-area: banner;
}

.main__row__banner img {
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

.main__card {
    min-width: 300px;
    width: 100%;
    min-height: 215px;
    height: 100%;
    background-color: #E8E9EB;
    padding: 25px 30px;
    border-radius: 5px;
    position: relative;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

.main__card.one {
    grid-area: card;
}

.main__card.two {
    grid-area: card2;
}

.main__row-2 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1fr;
    grid-column-gap: 2.5rem;
    grid-row-gap: 2.5rem;
    grid-template-areas: "card3 card4 card5";
    margin: 2.5rem 0;
}

.main__card.third {
    grid-area: card3;
}

.main__card.fourth {
    grid-area: card4;
}

.main__card.fifth {
    grid-area: card5;
}

.main__card-img {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 10rem;
    height: 8rem;
    padding: 0.5rem;
    object-fit: cover;
}
</style>
