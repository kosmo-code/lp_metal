<template>
  <div class="hero">
      <div class="hero-content">
          <h1 class="hero-content__title">Крупнейший металлмаркет России</h1>
          <p class="hero-content__description">Металлопрокат, трубы, лист...</p>
      </div>
      <button class="hero__btn btn__cta">Оставить заявку</button>
  </div>
</template>

<script>
export default {
    name: "TheHero",
}
</script>

<style lang="scss" scoped>
@import "assets/styles/index";

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  color: #FFFFFF;
  background: linear-gradient(rgba(0, 0, 0, 0.527),rgba(0, 0, 0, 0.5)), url("@/assets/images/hero.jpg") no-repeat;
  background-size: cover;
  object-fit: cover;
  height: calc(98vh - 5.625rem);
  &-content {
    padding-top: 4rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    line-height: 1.5;
    &__title {
      font-size: 3.5rem;
      font-weight: 700;
      margin-bottom: 0.75rem;
    }
    &__description {
      font-size: 1.5rem;
      font-weight: 500;
      letter-spacing: .75px;
      margin-bottom: 5rem;
    }
  }
  &__btn {
    font-size: 1.5rem;
    text-transform: uppercase;
  }
}
</style>
