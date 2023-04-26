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

$lightgrey: #F8F8F8;

.header {
    height: 5rem;
    padding: 0 2rem;
    position: fixed;
    z-index: 20;
    top: 0;
    left: 0;
    right: 0;
    background-color: #fff;
    border-bottom: 1px solid #eaecef;
    width: 100vw;
    font-size: 18px;
    font-weight: 500;
}

.header-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 5rem;
}

.header-menu {
    display: flex;
    gap: 1.2rem;
    align-items: flex-start;
    &__item:hover,
    &__link:hover {
        color: red;
        transition: color .5s ease;
    }
}

.logo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-left: 2rem;
    margin-right: 2rem;
}

.header-menu__contacts {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
}
.header-menu__contacts__list:not(:last-child) {
    margin-bottom: 0.3rem;
}

@media screen and (max-width: 1200px) {
    .header-menu {
        flex-direction: column;
        align-items: center;
        color: black;
        background: white;
        position: absolute;
        top: 4rem;
        left: 0;
        right: 0;
        width: 100vw;
        height: 100vh;
        padding: 50px;
        transform: translateX(-100%);
        transition: transform 1s;
    }
    .header-menu--active {
        transform: translateX(0);
    }
    .header-menu__contacts {
        width: 100%;
        align-items: flex-end;
    }
}

</style>
