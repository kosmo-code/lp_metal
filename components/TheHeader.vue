<template>
    <header class="header">
        <nav role="navigation" class="header-nav wrapper">
            <ul class="header-nav__list">
                <li class="header-nav__list__item">
                    <NuxtLink to="/" class="header-nav__list__item-link logo">
                        LOGO_M
                    </NuxtLink>
                </li>
                <li class="header-nav__list__item">
                    <NuxtLink to="/" class="header-nav__list__item-link btn__cta">
                        Консультация
                    </NuxtLink>
                </li>
                <li class="header-nav__list__item">
                    <NuxtLink to="/" class="header-nav__list__item-link">
                        Каталоги
                    </NuxtLink>
                </li>
                <li class="header-nav__list__item">
                    <NuxtLink to="/" class="header-nav__list__item-link">
                        Контакты
                    </NuxtLink>
                </li>
            </ul>
            <ul class="header-nav__list__right">
                <li class="header-nav__list__right__item">
                    <NuxtLink to="" class="header-nav__list__right__item-link">
                        Краснодар &dtrif;
                    </NuxtLink>
                    <ul class="dropdown">
                        <li><NuxtLink to="#">Сочи</NuxtLink></li>
                        <li><NuxtLink to="#">Ростов-на-Дону</NuxtLink></li>
                        <li><NuxtLink to="#">Махачкала</NuxtLink></li>
                        <li><NuxtLink to="#">Ставрополь</NuxtLink></li>
                    </ul>
                </li>
                <li class="header-nav__list__right__item">
                    <NuxtLink to="" class="header-nav__list__right__item-link">
                        8 901 234 56 78
                    </NuxtLink>
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

.header:before,
.header:after {
    content: " ";
    display: table;
}
.header:after {
    clear: both;
}

.header {
    top: 0;
    left: 0;
    position: fixed;
    background: #F8F8F8;
    z-index: 2;
    box-shadow: 0 4px 4px rgba(0,0,0,0.1);
    height: 5.625rem;
    width: 100%;
    padding: 2rem 0;
    //box-shadow: rgba(50, 50, 93, 0.25) 0 6px 12px -2px, rgba(0, 0, 0, 0.3) 0 3px 7px -3px;
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
