<template>
    <header class="header">
        <nav role="navigation" class="header-nav wrapper">
            <ul class="header-nav__list">
                <li class="header-nav__list__item">
                    <a href="" class="header-nav__list__item-link logo">
                        LOGO_M
                    </a>
                </li>
                <li class="header-nav__list__item">
                    <a href="" class="header-nav__list__item-link btn__cta">
                        Консультация
                    </a>
                </li>
                <li class="header-nav__list__item">
                    <a href="" class="header-nav__list__item-link">
                        Каталоги
                    </a>
                </li>
                <li class="header-nav__list__item">
                    <a href="" class="header-nav__list__item-link">
                        Контакты
                    </a>
                </li>
            </ul>
            <ul class="header-nav__list__right">
                <li class="header-nav__list__right__item">
                    <a href="" class="header-nav__list__right__item-link">
                        Краснодар &dtrif;
                    </a>
                    <ul class="dropdown">
                        <li><a href="#">Черкессия</a></li>
                        <li><a href="#">Ростов-на-Дону</a></li>
                        <li><a href="#">Махачкала</a></li>
                        <li><a href="#">Ставрополь</a></li>
                    </ul>
                </li>
                <li class="header-nav__list__right__item">
                    <a href="" class="header-nav__list__right__item-link">
                        8 901 234 56 78
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default ({

});
</script>

<style scoped lang="scss">
@import "assets/styles/index";

$lightgrey: #F8F8F8;

.header {
    min-height: 5.625rem;
    height: 100%;
    width: 100%;
    padding: 2rem 0;
    box-shadow: rgba(50, 50, 93, 0.25) 0 6px 12px -2px, rgba(0, 0, 0, 0.3) 0 3px 7px -3px;
}
.header-nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.header-nav__list {
    display: flex;
    align-items: center;
}
.header-nav__list__item {
    margin-right: 3rem;
}
.header-nav__list__item-link {
    font-size: 16px;
    color: #000;
}
.header-nav__list__right {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.header-nav__list__right__item {
    display: block;
}
.header-nav__list__right__item:first-child {
    //display: flex;
    display: block;
    align-items: center;
    margin-right: 2rem;
}
</style>
