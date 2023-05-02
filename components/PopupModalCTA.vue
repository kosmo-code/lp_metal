<template>
    <teleport to="body">
        <div class="modal-overlay" @click.stop="hideForm">
            <div class="modal" @click.stop>
                <div class="modal__title">Оставьте заявку</div>
                <span class="modal__description">Свяжитесь с нами, наши менеджеры будут рады помочь вам</span>
                <form action="" class="request" @submit.prevent>
                    <div class="form-control">
                        <label class="request__label" for="name">Имя:</label>
                        <input class="request__input" type="text" id="name" name="name" required placeholder="Введите ваше имя">
                    </div>

                    <div class="form-control">
                        <label class="request__label" for="email">Email:</label>
                        <input class="request__input" type="text" id="email" name="email" required placeholder="Введите вашу почту">
                    </div>

                    <div class="form-control">
                        <label class="request__label" for="phone">Номер телефона: </label>
                        <input class="request__input" type="tel" id="phone" name="phone" required placeholder="Введите ваш номер телефона">
                    </div>

                    <button type="submit" class="btn__cta-contacts mt-4">Отправить заявку</button>
                </form>
            </div>
            <!-- ./modal -->
            <div class="close">
                <img class="close-img" src="/close.svg" alt="Close image" />
            </div>
        </div>
    </teleport>
</template>

<script>
export default {
    name: "PopupModalCta",
    emits: ["onCloseForm", "hideForm"],
    setup(props, { emit }) {
        const hideForm = () => {
            emit("hideForm", false);
        };

        onBeforeMount(() => {
            emit("onCloseForm");
        });

        return { hideForm };
    },
}
</script>

<style lang="scss" scoped>
@import "assets/styles/index";

.mt-4 {
    margin-top: 4rem;
}
.modal-overlay {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  background-color: #000000da;
}

.modal {
  text-align: center;
  background-color: white;
  height: 350px;
  width: 700px;
  margin-top: 10%;
  padding: 60px 0;
  border-radius: 20px;
}
.modal__title {
    font-size: 2.5rem;
    line-height: 1.5;
    font-weight: 700;
}
.modal__description {
    font-size: 1.25rem;
    line-height: 1.5;
}
.request {
    margin: 1rem;
    padding-top: 1rem;
}
.close {
  margin: 10% 0 0 16px;
  cursor: pointer;
}

.close-img {
  width: 25px;
}

.form-control {
    position: relative;
    margin-bottom: 0.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 1rem;
}
.form-control input,
.form-control select {
    font-family: Inter, Roboto, Oxygen, Fira Sans, Helvetica Neue, sans-serif;
    margin: 0;
    outline: none;
    border: 2px solid #ccc;
    display: block;
    width: 300px;
    color: #2c3e50;
    padding: 0.5rem 1rem;
    border-radius: 3px;
    font-size: 1rem;
    resize: none;
}
</style>
