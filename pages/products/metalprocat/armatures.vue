<template>
    <div>
        <h3 class="armatures__title">Арматура</h3>
        <div class="armatures__info__props">
            <div class="armatures__info__props-material">
                <span>Материал: </span>
                <select name="material" id="material">
                    <option value="metal">Металлическая</option>
                    <option value="composite">Композитная</option>
                    <option value="fiberglass">Стеклопластиковая</option>
                    <option value="basaltplastic">Базальтопластиковая</option>
                </select>
            </div>
            <!-- /.armatures__info__material -->

            <div class="armatures__info__props-diameter">
                <span>Диаметр: </span>
                <select name="diameter" id="diameter">
                    <option value="six" selected>6 мм</option>
                    <option value="eight">8 мм</option>
                    <option value="ten">10 мм</option>
                    <option value="twelve">12 мм</option>
                    <option value="fourteen">14 мм</option>
                    <option value="sixteen">16 мм</option>
                    <option value="twenty">20 мм</option>
                </select>
            </div>
            <!-- /.armatures__info__diameter -->

            <div class="armatures__info__props-class">
                <span>Класс: </span>
                <select name="class" id="class">
                    <option value="А240" selected>А240 (АI, А1)</option>
                    <option value="А400"> А400 (АIII, А3)</option>
                    <option value="А500С">А500С</option>
                </select>
            </div>
            <!-- /.armatures__info__class -->

            <div class="armatures__info__props-surface">
                <span>Поверхность: </span>
                <select name="surface" id="surface">
                    <option value="smooth" selected>Гладкая</option>
                    <option value="corrugated">Рифленая</option>
                </select>
            </div>
            <!-- /.armatures__info__surface -->
        </div>
        <button class="btn__cta mt-2">Рассчитать стоимость</button>
    </div>
</template>

<script>

export default {
    name: "armatures",
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

        definePageMeta({
           layout: "category-detail"
        });

        return {
            armaturesList,
        };
    },
}
</script>

<style scoped lang="scss">
@import "assets/styles/index";

.mt-2 {
    margin-top: 2rem;
}

.armatures {
    max-width: 1000px;
    margin: 0 auto;
    padding: 6rem;
    display: block;
    opacity: 1;
    background-color: rgb(255, 255, 255);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    box-sizing: border-box;
    border: 1px solid #e5e7eb;
}
.armatures__wrapper {
    display: grid;
    padding: 2rem;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    max-width: 80rem;
    margin: 0 auto;
}
.armatures__info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}
.armatures__title {
    font-size: 2.25rem;
    line-height: 2.5;
    font-weight: 700;
    letter-spacing: -0.025rem;
}
.armatures__info__props {
    border: 1px solid #DDD;
    border-radius: 8px;
    padding: .5rem 2rem 0 .5rem;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

.armatures__info__props-material,
.armatures__info__props-diameter,
.armatures__info__props-class,
.armatures__info__props-surface {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
    font-weight: 600;
    & span {
        margin-right: 1rem;
    }
    & select {
        border: 1px solid #DDD;
        border-radius: 5px;
        background: #F8F8F8;
    }
}
</style>
