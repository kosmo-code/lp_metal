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

<style scoped lang="css">

.contacts {
    min-height: calc(100vh - 9.5rem);
    background: linear-gradient(rgba(0, 0, 0, 0.5),rgba(0, 0, 0, 0.9)), url("assets/images/callCenter.jpg") no-repeat gray;
    background-size: cover;
    object-fit: cover;
    color: #fff;
}
.contacts__content {
    max-width: 1095px;
    width: 100%;
    padding: 0 4rem;
    margin: 0 auto;
}
.contacts__content-text {
    padding-top: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 2rem;
}

.contacts__content-text__title {
    font-size: 3.5rem;
    line-height: 1.5;
}
.contacts__content-text__description {
    font-size: 1.2rem;
    margin-top: -1.5rem;
    margin-bottom: 2rem;
}
.contacts__content-bottom {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
}
.contacts__content-bottom__title {
    font-size: 1.5rem;
    font-weight: 600;
    margin-bottom: 2rem;
}


.feedback {
    background-color: transparent;
    opacity: 95%;
    max-width: 600px;
    box-shadow: 0 0 10px rgba(0,0,0,0.2);
    border-radius: 5px;
}
.feedback__label {
    display: block;
    margin-bottom: 10px;
    font-weight: bold;
    background-color: transparent;
}

.feedback__input, textarea {
    background-color: white;
    width: 100%;
    padding: 10px;
    border-radius: 5px;
    font-size: 1rem;
    font-weight: 500;
    margin-bottom: 20px;
    box-sizing: border-box;
    color: #000000;
    border: 1px solid transparent;
}
.feedback__input:focus,
textarea:focus {
    padding-top: 20px;
    transition: all .5s;
    border: 2px solid red;
    outline: red;
}

.feedback__btn {
    min-width: 10rem;
    display: none;
    padding: 0.5rem 1rem;
    margin: 2rem auto;
    border: 1px solid #fff;
    cursor: pointer;
    background: red;
    color: #FFFFFF;
    &:hover {
        text-decoration: underline;
        transition: all 1s ease-out;
    }
}

.btn__cta-contacts {
    margin: 2rem 0;
    opacity: 1;
    font-size: 1.5rem;
    background: red;
    padding: 0.5rem 1rem;
    color: #FFFFFF;
    &:hover,
    &:focus {
        opacity: 0.85;
        transition: all .8s ease;
        cursor: pointer;
        text-decoration: underline;
    }
}

textarea {
    height: 150px;
}

input[type="submit"] {
    background-color: transparent;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
}

.contacts__content-bottom-right {
    padding: 0 2rem;
    margin: 0 4rem;
}

.contacts__content-bottom-right__title {
    font-size: 14px;
    font-weight: 700;
    color: #868686;
}
.contacts__content-bottom-right__description {
    font-size: 1.2rem;
    line-height: 1.5;
}

@media screen and (max-width: 756px) {
    .contacts__content-bottom {
        display: flex;
        flex-direction: column-reverse;
        align-items: center;
        justify-content: center;
    }
    .contacts__content-bottom-right {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(3, 1fr);
        gap: 0 1rem;
        align-items: center;
    }
    .contacts__content-bottom__title {
        grid-column-start: span 3;
    }
    .contacts__content-bottom-right__title {
        grid-row-start: span 1;
        grid-column-start: span 1;
    }
    .contacts__content-bottom-right__description.address {
        grid-row-start: span 1;
        grid-column-start: span 2;
    }
    .contacts__content-bottom-right__description.tel {
        grid-row-start: span 1;
        grid-column-start: span 2;
    }
    .contacts__content-bottom-right__description.email {
        grid-row-start: span 1;
        grid-column-start: span 2;
    }
    .contacts__content-bottom-left {
        display: none;
    }
    .feedback__btn {
        display: block;
    }
}
</style>
