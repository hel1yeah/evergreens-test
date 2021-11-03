<template>
  <div class="container">
    <nav class="nav-page">
      <ul class="nav-page__list">
        <li class="nav-page__list-item">
          <a href="#" class="nav-page__list-item-link">Нагро удобрение </a>
        </li>
        <li class="nav-page__list-item">
          <a href="#" class="nav-page__list-item-link">Биодизель</a>
        </li>
        <li class="nav-page__list-item">
          <a href="#" class="nav-page__list-item-link">Силко</a>
        </li>
        <li class="nav-page__list-item">
          <a href="#" class="nav-page__list-item-link">Интернет-магазин</a>
        </li>
        <li class="nav-page__list-item">
          <a href="#" class="nav-page__list-item-link">Вопросы-ответы</a>
        </li>
        <li class="nav-page__list-item">
          <a href="#" class="nav-page__list-item-link">Контакты</a>
        </li>
      </ul>
      <button class="nav-page__baskets">
        <img
          class="nav-page__baskets-img"
          src="./../assets/images/baskets.svg"
          alt="baskets"
        />
        <span class="nav-page__baskets-descr">Корзина</span>
      </button>
    </nav>
  </div>
</template>

<script>
export default {
  name: "TheNav",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/scss/_mixin.scss";

.nav-page {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: $white;
  border: 1px solid $white;
}
.nav-page__list {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  padding: 0 24px 0 42px;
}
.nav-page__list-item {
  // width: 120px;
}
.nav-page__list-item-link {
  font-family: "Roboto Condensed", serif;
  font-size: 14px;
  color: $grey;
  position: relative;
  text-transform: uppercase;
  &:before {
    position: absolute;
    content: "";
    width: 3px;
    height: 6px;
    top: 32%;
    // transform: translateY(-50%);
    right: -10px;
    background-image: url("../assets/images/triangle.svg");
  }
}
.nav-page__baskets {
  border: transparent;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 47px;
  width: 148px;
  cursor: pointer;
  background: rgb(117, 91, 30);
  background: linear-gradient(0deg, $brown 0%, $green 100%);
  transition: all 0.5s ease-out;
  &:hover {
    transform: translateY(-5px);
  }
}

.nav-page__baskets-img {
  width: 9.5px;
  height: 8px;
  border: 1px solid $grey;
  border-radius: 50%;
}
.nav-page__baskets-descr {
  color: $white;
  text-transform: uppercase;
}

@media screen and (max-width: 850px) {
  .nav-page__list {
    max-width: 465px;
    flex-wrap: wrap;
    padding: 0 0 0 5px;
  }
  .nav-page__list-item {
    width: 120px;
  }
  .nav-page__baskets {
    margin: 0 5px 0 0;
  }
}
</style>
