<template>
    <div class="contacts">
        <div class="contacts__content">
            <div class="contacts__content-text">
                <h1 class="contacts__content-text__title" id="contacts">Контакты</h1>
                <p class="contacts__content-text__description">Свяжитесь с нами, наши менеджеры будут рады вам помочь.</p>
            </div>
            <div class="contacts__content-bottom">
                <div class="contacts__content-bottom-left">
                    <div class="contacts__content-bottom__title">Обратная связь</div>
                    <form action="" class="feedback">
                        <label class="feedback__label" for="name">Имя:</label>
                        <input class="feedback__input" type="text" id="name" name="name" required placeholder="Введите ваше имя">

                        <label class="feedback__label" for="email">Email:</label>
                        <input class="feedback__input" type="text" id="email" name="email" required placeholder="Введите вашу почту">

                        <label class="feedback__label" for="phone">Номер телефона: </label>
                        <input class="feedback__input" type="tel" id="phone" name="phone" required placeholder="Введите ваш номер телефона">

                        <button type="submit" class="btn__cta-contacts">Отправить заявку</button>
                    </form>
                </div>
                <div class="contacts__content-bottom-right">
                    <div class="contacts__content-bottom__title">Контактная информация</div>
                    <span class="contacts__content-bottom-right__title">АДРЕС</span>
                    <p class="contacts__content-bottom-right__description address">196240, Ростов-на-Дону, <br>6-ой Предпортовый проезд, 12</p>
                    <span class="contacts__content-bottom-right__title">ТЕЛЕФОНЫ</span>
                    <p class="contacts__content-bottom-right__description tel">8 (812) 222-33-22</p>
                    <span class="contacts__content-bottom-right__title">ЭЛЕКТРОННАЯ ПОЧТА</span>
                    <p class="contacts__content-bottom-right__description email">contact@mc.ru</p>
                    <button class="feedback__btn">Оставить заявку</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TheContacts",
}
</script>

<style scoped lang="scss">
@import "assets/styles/index";
</style>
