<template>
  <section class="calculator">
    <div class="calculator__card">
      <div class="calculator__card-inner">
        <h2 class="calculator__card-title">Посчитайте прибыль <br /></h2>
        <span class="calculator__card-descr">добриво эфективнее химии</span>
        <div class="calculator__card-wrapper">
          <label class="calculator__card-label">
            <span class="calculator__card-title-input">Выберите культуру</span>
            <select class="calculator__card-select">
              <option class="calculator__card-option" value="3100">
                Пшеница ≈ 3100 грн / т
              </option>
              <option class="calculator__card-option" value="1100">
                Кукурудза ≈ 1100 грн / т
              </option>
              <option class="calculator__card-option" value="2300">
                Ячмень ≈ 2300 грн / т
              </option>
              <option class="calculator__card-option" value="1800">
                Овес ≈ 1800 грн / т
              </option>
              <option class="calculator__card-option" value="970">
                Рож ≈ 970 грн / т
              </option>
              <option class="calculator__card-option" value="2600">
                Просо ≈ 2600 грн / т
              </option>
              <option class="calculator__card-option" value="4400">
                Гречиха ≈ 4400 грн / т
              </option>
            </select>
          </label>
          <label class="calculator__card-label">
            <span class="calculator__card-title-input">Урожайность, ц/га</span>
            <input type="text" class="calculator__card-input" />
          </label>
          <label class="calculator__card-label">
            <span class="calculator__card-title-input"
              >Стоимость хим. удобрения, грн/га</span
            >
            <input type="text" class="calculator__card-input" />
          </label>
          <label class="calculator__card-label">
            <span class="calculator__card-title-input"
              >Посевная площадь, га</span
            >
            <input type="text" class="calculator__card-input" />
          </label>
        </div>

        <h4 class="calculator__card-profit">Прибыль от добрива</h4>
        <h4 class="calculator__card-res">50 000</h4>
        <span class="calculator__card-currency">грн</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TheCalculator",
};
</script>

<style lang="scss" scoped>
@import "./../assets/scss/_mixin.scss";
.calculator {
  width: 520px;
  height: 590px;
  background-image: url("./../assets/images/preparation.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 0 0;
}
.calculator__card {
  background-color: $lite-grey;
  padding: 15px 13px;
  max-width: 320px;
  color: $dark-grey;
  margin: -182px 72px;
}
.calculator__card-inner {
  border: 1px dashed $dark-grey;
  border-radius: 2px;
  padding: 22px 24px 18px;
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: $white;
}
.calculator__card-title {
  font-family: "Roboto Condensed", sans-serif;
  font-size: 36px;
  line-height: 32px;
  text-transform: uppercase;
  font-weight: 100;
  text-align: center;
}
.calculator__card-descr {
  font-family: "RobotoLight", sans-serif;
  font-size: 14px;
  line-height: 18px;
  font-weight: 800;
  text-transform: uppercase;
  margin: 20px 0 0 0;
  background: $pink;
}

.calculator__card-wrapper {
  margin: 50px 0 25px;
  position: relative;
  width: 100%;
  &::before {
    position: absolute;
    content: "";
    top: -36px;
    left: 50%;
    transform: translateX(-50%);
    width: 69%;
    height: 1px;
    border-top: 1px solid $grey-low;
  }
  &::after {
    position: absolute;
    content: "";
    bottom: -15px;
    left: 50%;
    transform: translateX(-50%);
    width: 69%;
    border-top: 1px solid $grey-low;
  }
}
.calculator__card-label {
}
.calculator__card-title-input {
  font-family: "RobotoLight", sans-serif;
  font-size: 14px;
  line-height: 18px;
  display: block;
  width: 100%;
  margin: 18px 0 0 0;
}
.calculator__card-select {
  width: 100%;
  height: 30px;
  border: 1px solid $grey-low;
  margin: 8px 0 0 0;
}
.calculator__card-option {
}
.calculator__card-input {
  width: 100%;
  height: 30px;
  margin: 8px 0 0 0;
}
.calculator__card-profit {
  background: $pink;
  color: $red;
  font-family: "RobotoLight", sans-serif;
  font-size: 14px;
  line-height: 20px;
}
.calculator__card-res {
  margin: 19px 0 0 0;
  font-family: "Roboto Condensed", sans-serif;
  font-size: 47px;
  line-height: 38px;
  color: $red;
}
.calculator__card-currency {
  font-family: "RobotoLight", sans-serif;
  font-size: 14px;
  line-height: 20px;
}
</style>
