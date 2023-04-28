<template>
    <header class="header">
        <div class="wrapper">
            <div class="burger-menu">
                <input type="checkbox" id="menu-toggle" @click="toggleMenuBtn"/>
                <label for="menu-toggle"></label>
            </div>
            <nav role="navigation" class="header-nav">
                <ul class="header-menu" id="menu" :class="{ 'header-menu--active': menuBtn }">
                    <li>
                        <NuxtLink to="/" class="logo">
                            LOGO_M
                        </NuxtLink>
                    </li>
                    <li class="header-menu__item">
                        <NuxtLink to="/" class="header-menu__link">
                            Главная
                        </NuxtLink>
                    </li>
                    <li class="header-menu__item">
                        <NuxtLink to="/products/all" class="header-menu__link">
                            Каталоги
                        </NuxtLink>
                    </li>
                    <li class="header-menu__item">
                        <NuxtLink :to="{ hash: '#contacts' }" class="header-menu__link">
                            Контакты
                        </NuxtLink>
                    </li>
                </ul>

                <ul class="header-menu__contacts">
                    <li class="header-menu__contacts__list">
                        <NuxtLink to="" class="header-menu__contacts__link">
                            8 901 234 56 78
                        </NuxtLink>
                    </li>
                    <li class="header-menu__contacts__list">
                        <NuxtLink to="" class="header-menu__contacts__link">
                            Краснодар &dtrif;
                        </NuxtLink>
                        <ul class="dropdown">
                            <li><NuxtLink to="">Сочи</NuxtLink></li>
                            <li><NuxtLink to="">Ростов-на-Дону</NuxtLink></li>
                            <li><NuxtLink to="">Махачкала</NuxtLink></li>
                            <li><NuxtLink to="">Ставрополь</NuxtLink></li>
                        </ul>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    setup() {
        const menuBtn = ref(false);
        const toggleMenuBtn = () => {
            menuBtn.value = !menuBtn.value;
        }

        return {
            menuBtn,
            toggleMenuBtn,
        };
    },
};
</script>

<style scoped lang="scss">
@import "assets/styles/index";
</style>
