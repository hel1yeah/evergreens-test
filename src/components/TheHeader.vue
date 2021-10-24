<template>
  <header class="header">
    <img class="header__logo" src="../assets/images/logo.png" alt="Добриво" />
    <div class="header__inner">
      <nav class="header__nav">
        <ul class="header__nav-list">
          <li class="header__nav-list-item">
            <a class="header__nav-list-link" href="#">Оплата и Доставка</a>
          </li>
          <li class="header__nav-list-item">
            <a class="header__nav-list-link" href="#">Новости</a>
          </li>
          <li class="header__nav-list-item">
            <a class="header__nav-list-link" href="#">Справочник</a>
          </li>
          <li class="header__nav-list-item">
            <a class="header__nav-list-link" href="#">Сертификаты</a>
          </li>
        </ul>
      </nav>
      <div class="header__language-selection">ru</div>
    </div>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
};
</script>

<style lang="scss" scoped>
@import "./../assets/scss/_mixin.scss";
.header {
  max-width: 1020px;
  padding: 90px 10px 0;

  margin: 0 auto;
  display: flex;
  align-content: center;
  justify-content: space-between;
}
.header__logo {
  max-width: 221px;
  max-height: 43px;
}
.header__inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 545px;
  color: $white;
  text-transform: uppercase;
}
.header__nav {
  width: 440px;
}
.header__nav-list {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.header__nav-list-item {
}
.header__nav-list-link {
  color: $white;
  font-size: 11px;
  line-height: 17px;
  font-family: "RobotoLight", serif;
}
.header__language-selection {
  width: 42px;
  height: 21px;
  padding: 0 0 0 8px;
  font-size: 14px;
  border: 1px solid $white;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  position: relative;
  cursor: pointer;
  &::before {
    content: "";
    position: absolute;
    width: 6px;
    height: 3px;
    top: 50%;
    transform: translateY(-50%);
    right: 6px;
    background-image: url("./../assets/images/arrow.png");
    background-position: center center;
    background-size: cover;
    background-repeat: no-repeat;
  }
}
</style>
