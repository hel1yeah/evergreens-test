<template>
  <section class="descr">
    <h1 class="descr__title">
      Органическоре
      <span>нано-удобрение</span>
      <br />
      <span>добриво</span>
    </h1>
    <div class="descr__capability">
      <img class="descr__img" src="./../assets/images/means.png" alt="means" />
      <div class="descr__text">
        <ul class="descr__list">
          <li class="descr__list-item">
            <h3 class="descr__list-item-header">Прирост урожая</h3>
            <span class="descr__list-item-explanation">
              в сравнении с химическим удобрением
            </span>
            <span class="descr__list-item-percent">30%-250%</span>
          </li>
          <li class="descr__list-item">
            <h3 class="descr__list-item-header">Экономия</h3>
            <span class="descr__list-item-explanation">
              химических удобрений в хозяйстве
            </span>
            <span class="descr__list-item-percent"> до 70% </span>
          </li>
          <li class="descr__list-item">
            <h3 class="descr__list-item-header">Рост корневой</h3>
            <span class="descr__list-item-explanation">
              системы растений при использовании
            </span>
            <span class="descr__list-item-percent">в 3-10раз</span>
          </li>
        </ul>
      </div>
    </div>
    <div class="descr__to-order">
      <div class="descr__to-order-text-aside">Хотитите трали-вали ла-лала</div>
      <h2 class="descr__to-order-text">
        Узнайте <br />
        о нагро больше!
      </h2>
      <button class="descr__button">
        <span class="descr__button-text">Узнать больше</span>
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: "TheDescr",
};
</script>

<style lang="scss" scoped>
@import "./../assets/scss/_mixin.scss";
.descr {
  margin: 93px 0 0 0;
  max-width: 731px;
}
.descr__title {
  font-family: "Roboto Condensed", serif;
  text-transform: uppercase;
  font-weight: 300;
  font-size: 60px;
  line-height: 48px;
  color: $white;
  max-width: 535px;
  margin: 0 0 0 81px;
}

.descr__title span:first-child {
  margin: 0 0 0 100px;
  white-space: nowrap;
}
.descr__title span:last-child {
  margin: 0 0 0 151px;
}
.descr__capability {
  display: flex;
  margin: -40px 0 0 13px;
}
.descr__img {
  width: 190px;
  height: 345px;
}
.descr__text {
  margin: 64px 0 0 0;
}
.descr__list {
}
.descr__list-item {
  padding: 27px 0 0 82px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  position: relative;
  &::before {
    content: "";
    position: absolute;
    top: 18px;
    left: 34px;
    width: 33px;
    height: 33px;
    background-image: url("./../assets/images/star.png");
    background-position: center center;
    background-size: cover;
    background-repeat: no-repeat;
  }
}
.descr__list-item-header {
  color: $black;
  text-transform: uppercase;
  font-family: "Roboto Condensed", sans-serif;
  font-weight: 100;
  font-size: 25px;
  line-height: 19px;
}
.descr__list-item-explanation {
  margin: 10px 0 0 0;
  color: $grey;
  font-family: "Roboto", sans-serif;
  font-size: 11px;
  line-height: 13px;
}
.descr__list-item-percent {
  margin: 10px 0 0 0;
  color: $orage;
  font-family: "Roboto", sans-serif;
  font-size: 25px;
  line-height: 19px;
}

.descr__to-order {
  float: right;
  position: relative;
  text-transform: uppercase;
}
.descr__to-order-text {
  font-size: 42px;
  line-height: 50px;
  font-family: "Roboto Condensed", sans-serif;
  color: $blue;
  font-weight: 100;
  margin: 56px 60px 0 0;
}
.descr__to-order-text-aside {
  position: absolute;
  top: 66px;
  left: -110px;
  font-family: "Roboto", sans-serif;
  line-height: 17px;
  font-size: 14px;
  font-weight: normal;
  max-width: 80px;
  color: #25383f;
  text-transform: lowercase;
  text-align: right;
  &::first-letter {
    text-transform: uppercase;
  }
}
.descr__button {
  border: 5px solid $black;
  background-color: transparent;
  margin: 30px 0 0 0;
  padding: 16px 28px;
  cursor: pointer;
  transition: 0.5s;
  text-transform: uppercase;
  &:hover {
    transform: translateY(-10px);
  }
}
.descr__button-text {
  font-family: "RobotoLight", sans-serif;
  font-size: 23px;
  line-height: 27px;
  background-color: $pink;
}

@media screen and (max-wight: 768px) {
  .descr__capability {
    justify-content: center;
    margin: 0px 0px 0px 0px;
  }
}
</style>
