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
                            <div class="products__content__card-img">
                                <img class="" src="/armatures.png" alt="Armatures Category Image">
                            </div>
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
                            <div class="products__content__card-img">
                                <img class="" src="/truba.png" alt="Photo of category">
                            </div>
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
                            <div class="products__content__card-img">
                                <img class="" src="/list.png" alt="Photo of category">
                            </div>
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
                            <div class="products__content__card-img">
                                <img class="" src="/setka.png" alt="Photo of category">
                            </div>
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
                            <div class="products__content__card-img">
                                <img class="" src="/threeDots.svg" alt="Photo of category">
                            </div>
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
</style>
