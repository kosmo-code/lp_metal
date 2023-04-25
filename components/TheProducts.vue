<template>
    <div>
        <section class="products">
            <div class="wrapper">
                <div class="products__content">
                    <!-- col-1 -->
                    <div class="products__content__banner">
                        <img src="/products-banner.jpg" alt="Banner">
                        <div class="products__content__banner-bottom">
                            <span class="products__content__banner-bottom-text">Быстрая доставка в день обращения</span>
                            <div class="products__content__banner-bottom-buttons">
                                <button class="btn__cta">Быстрый заказ</button>
                                <!-- Добавить динамический класс цвета -->
                                <NuxtLink class="btn__link" to="/products/all">Весь каталог</NuxtLink>
                            </div>
                        </div>
                    </div>
                    <div class="products__content__card">
                        <NuxtLink to="">
                            <img class="products__content__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="Photo of category">
                            <h3 class="products__content__card-title">Мателлопрокат</h3>
                            <p>Арматура</p>
                            <p>Квадрат</p>
                            <p>Круг</p>
                        </NuxtLink>
                        <!-- Добавить динамический класс цвета -->
                        <NuxtLink class="btn__link red" to="">все категории</NuxtLink>
                    </div>
                    <!-- /col-1 -->

                    <!-- col-2 -->
                    <div class="products__content__card">
                        <NuxtLink to="">
                            <img class="products__content__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="Photo of category">
                            <h3 class="products__content__card-title">Труба</h3>
                            <p>Труба круглая</p>
                            <p>Труба профильная</p>
                            <p>Труба квадратная</p>
                        </NuxtLink>
                        <!-- Добавить динамический класс цвета -->
                        <NuxtLink class="btn__link red" to="">все категории</NuxtLink>
                    </div>
                    <!-- /col-2 -->

                    <!-- col-3 -->
                    <div class="products__content__card">
                        <NuxtLink to="">
                            <img class="products__content__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="Photo of category">
                            <h3 class="products__content__card-title">Лист</h3>
                            <p>Лист гладкий</p>
                            <p>Лист рифленый</p>
                            <p>Лист перфорированный</p>
                        </NuxtLink>
                        <!-- Добавить динамический класс цвета -->
                        <NuxtLink class="btn__link red" to="">все категории</NuxtLink>
                    </div>
                    <div class="products__content__card">
                        <NuxtLink to="">
                            <img class="products__content__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="Photo of category">
                            <h3 class="products__content__card-title">Сетка</h3>
                            <p>Сетка рабица</p>
                            <p>Сетка тканая</p>
                            <p>Сетка сварная</p>
                        </NuxtLink>
                        <!-- Добавить динамический класс цвета -->
                        <NuxtLink class="btn__link red" to="">все категории</NuxtLink>
                    </div>
                    <div class="products__content__card">
                        <NuxtLink to="">
                            <img class="products__content__card-img" src="https://mb1.ru/upload/iblock/c13/d5tl9pv0oj6kci93krsafkg1czi35o6s.png" alt="Photo of category">
                            <h3 class="products__content__card-title">Проволока</h3>
                            <h3 class="products__content__card-title">Трубопроводная арматура</h3>
                            <h3 class="products__content__card-title">АТИ</h3>
                            <h3 class="products__content__card-title">...</h3>
                        </NuxtLink>
                        <!-- Добавить динамический класс цвета -->
                        <NuxtLink class="btn__link red" to="">все категории</NuxtLink>
                    </div>
                    <!-- /col-3 -->
                </div>
                <!-- /.products__content -->
            </div>
            <!-- /.wrapper -->
        </section>
        <!-- /.products -->
    </div>
</template>

<script>
export default {
    name: "TheProducts",
}
</script>

<style scoped lang="scss">
@import "assets/styles/index";

.products {
    width: 100%;
    left: 0;
    right: 0;
    top: 0;
    min-height: 100vh;
    margin: 2rem 0;
}

.products__content {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 1.5rem 2rem;
}

.products__content__banner {
    grid-column-start: span 2;
    grid-row-start: span 2;

    background-color:rgba(0,0,0,.8);

    position: relative;
    text-align: center;
    max-width: 100%;
}

.products__content__banner img {
    opacity: 35%;

    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

.products__content__banner-bottom {
    color: #FFFFFF;
    position: absolute;
    width: 100%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    line-height: 1.5;
    letter-spacing: 0.5px;
    font-size: 24px;
}

.products__content__banner-bottom-text {
    font-weight: 600;
    line-height: 1.5;
    letter-spacing: 0.5px;
    font-size: 24px;
}

.products__content__banner-bottom-buttons {
    margin-top: 2rem;
}

.btn__link {
    padding: 0.5rem 1rem;
    background: transparent;
    border: 1px solid #fff;
    margin-left: 2rem;
    cursor: pointer;
    &:hover {
        text-decoration: underline;
        transition: all 2s ease-out;
    }
}
.btn__link.red {
    position: absolute;
    bottom: 1rem;
    left: 0;
    //padding: 0.5rem;
    background: red;
    color: #FFFFFF;
}

.products__content__card {
    position: relative;
    background-color: #E8E9EB;
    padding: 25px 30px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

.products__content__card-img {
    position: absolute;
    bottom: 0;
    right: 0;
    max-width: 10rem;
    height: 8rem;
    padding: 0.5rem;
    object-fit: cover;
}

.products__content__card-title {
    font-weight: 600;
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
}

@media screen and (max-width: 1200px) {
    .products__content {
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
        height: 100%;
    }
    .products__content__banner,
    .products__content__card {
        min-height: 12rem;
        width: 100%;
    }
}
@media screen and (max-width: 576px) {
    .products__content__banner-bottom-buttons {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
    }
    .products__content__banner-bottom-buttons button {
        margin-bottom: 1rem;
        margin-left: 2rem;
    }
}
</style>
