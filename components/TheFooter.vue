<template>
  <footer class="footer">
      <div class="wrapper">
          <ul class="footer__menu">
              <li>
                  <span>Официальный сайт</span>
                  <p>компании "LOGO_M"</p>
              </li>
              <li>
                  <a href="">Положение прав о защите персональных данных</a>
                  <p>Правовая информация</p>
              </li>
              <li>
                  <a href="">
                      Cookies
                  </a>
              </li>
          </ul>
      </div>
  </footer>
</template>

<script>
export default {
    name: "TheFooter",
}
</script>

<style scoped>
@import "assets/styles/index.css";
.footer {
  max-height: 90px;
  height: 100%;
  background: #F8F8F8;
  padding: 20px 0;
}
.footer__menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
