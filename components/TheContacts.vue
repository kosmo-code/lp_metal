<template>
    <div class="contacts my-5" ref="">
        <div class="contacts__content">
            <div class="contacts__content-text">
                <h1 class="contacts__content-text__title">Контакты</h1>
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

                        <button type="submit" class="my-5 _btn__cta">Отправить заявку</button>
                    </form>
                </div>
                <div class="contacts__content-bottom-right">
                    <div class="contacts__content-bottom__title">Контактная информация</div>
                    <span class="contacts__content-bottom-right__title">АДРЕС</span>
                    <p class="contacts__content-bottom-right__description">196240, Ростов-на-Дону, 6-ой Предпортовый проезд, 12</p>
                    <span class="contacts__content-bottom-right__title">ТЕЛЕФОНЫ</span>
                    <p class="contacts__content-bottom-right__description">8 (812) 222-33-22</p>
                    <span class="contacts__content-bottom-right__title">ЭЛЕКТРОННАЯ ПОЧТА</span>
                    <p class="contacts__content-bottom-right__description">contact@mc.ru</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TheContacts",
    setup() {
        // const parallaxContainer = ref(null);
        //
        // const handleScroll = () => {
        //     const offset = window.pageYOffset;
        //     parallaxContainer.value.style.backgroundPositionY = offset * 0.7 + 'px';
        // };
        //
        // onMounted(() => {
        //     window.addEventListener('scroll', handleScroll);
        // });
        //
        // return {
        //     parallaxContainer,
        //     handleScroll
        // };
    }
}
</script>

<style scoped lang="css">
.my-5 {
    margin: 4rem 0;
}
.contacts {
    height: calc(98vh - 5.625rem);
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
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 4rem;
}

.contacts__content-text__title {
    font-size: 3.375rem;
    line-height: 1.5;
}
.contacts__content-text__description {
    font-size: 1.2rem;
}
.contacts__content-bottom {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
}
.contacts__content-bottom__title {
    font-size: 1.5rem;
    font-weight: 600;
    margin-bottom: 1.2rem;
}
.feedback {
    background-color: transparent;
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
    background-color: transparent;
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 16px;
    font-weight: 500;
    margin-bottom: 20px;
    box-sizing: border-box;
    color: #FFFFFF;
}

._btn__cta {
    opacity: 1;
    font-size: 1.5rem;
    background: red;
    padding: 0.5rem 1rem;
    color: #FFFFFF;
    text-decoration: none;
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

}
.contacts__content-bottom-right__title {
    font-size: 14px;
    font-weight: 700;
    letter-spacing: 1.25px;
    color: #868686;
}
.contacts__content-bottom-right__description {
    line-height: 1.5;
}

.parallax-container {
    height: calc(98vh - 5.625rem);
    background: linear-gradient(rgba(0, 0, 0, 0.5),rgba(0, 0, 0, 0.9)), url("assets/images/callCenter.jpg") no-repeat gray;
    background-size: cover;
    object-fit: cover;
    overflow: hidden;
}

.parallax-content {
    position: relative;
    top: 50%;
    transform: translateY(-50%);
    text-align: center;
    color: #fff;
}
</style>
