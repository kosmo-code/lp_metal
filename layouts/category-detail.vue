<template>
    <div>
        <div class="go-back">
            <NuxtLink to="/products/all">&#8592; вернуться назад</NuxtLink>
        </div>
        <div class="category">
            <div class="category__wrapper">
                <div class="category__info">
                    <slot />
                </div>
                <div class="category__img">
                    <img src="/armatures-detail.png" alt="Category IMG">
                </div>
                <!-- /.category__info -->
            </div>
            <!-- /.category__wrapper -->
        </div>
    </div>
</template>

<script>
export default {
    name: "category-detail",
    setup() {
        // const goBack = () => {
        //     window.history.length > 1 ? this.$router.go(-1) : this.$router.push('/')
        // }
    },
}
</script>

<style lang="scss" scoped>
@import "assets/styles/index";

.go-back {
    width: 1000px;
    margin: 0 auto;
    padding: 5rem -0px;
}

.category {
    max-width: 1000px;
    //margin: 10rem auto 0;
    padding: 2rem;
    display: block;
    opacity: 1;
    background-color: rgb(255, 255, 255);
    //box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    box-sizing: border-box;
    border: 1px solid #e5e7eb;
    margin: 0 auto;
}
.category span {
    margin: 0 auto;
}
.category__wrapper {
    display: grid;
    align-items: center;
    //padding: 2rem;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    max-width: 80rem;
    width: 100%;
    margin: 0 auto;
}
.category__info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.category__img {
    //margin-right: 2rem;
}
</style>
