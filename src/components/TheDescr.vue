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
            <h2 class="descr__list-item-header">Прирост урожая</h2>
            <span class="descr__list-item-explanation">
              в сравнении с химическим удобрением
            </span>
            <span class="descr__list-item-percent">30%-250%</span>
          </li>
          <li class="descr__list-item">
            <h2 class="descr__list-item-header">Экономия</h2>
            <span class="descr__list-item-explanation">
              химических удобрений в хозяйстве
            </span>
            <span class="descr__list-item-percent"> до 70% </span>
          </li>
          <li class="descr__list-item">
            <h2 class="descr__list-item-header">Рост корневой</h2>
            <span class="descr__list-item-explanation">
              системы растений при использовании
            </span>
            <span class="descr__list-item-percent">в 3-10раз</span>
          </li>
        </ul>
      </div>
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
  // @include myFlex;
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
</style>
