<template>
  <section class="calculator">
    <div class="calculator__card">
      <div class="calculator__card-inner">
        <h2 class="calculator__card-title">Посчитайте прибыль <br /></h2>
        <span class="calculator__card-descr">добриво эфективнее химии</span>
        <div class="calculator__card-wrapper">
          <label class="calculator__card-label">
            <span class="calculator__card-title-input">Выберите культуру</span>
            <select
              class="calculator__card-select"
              v-model.number.trim="sowing"
            >
              <option class="calculator__card-option" value="3100">
                Пшеница ≈ 3100 грн / т
              </option>
              <option class="calculator__card-option" value="1100">
                Кукурудза ≈ 1100 грн / т
              </option>
              <option class="calculator__card-option" value="2300">
                Ячмень ≈ 2300 грн / т
              </option>
              <option selected class="calculator__card-option" value="1800">
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
            <input
              type="number"
              class="calculator__card-input"
              placeholder="20"
              v-model.number.trim="prolificness"
            />
            <div class="calculator__card-error" v-if="errors.prolificness">
              {{ errors.prolificness }}
            </div>
          </label>
          <div></div>
          <label class="calculator__card-label">
            <span class="calculator__card-title-input"
              >Стоимость хим. удобрения, грн/га</span
            >
            <input
              type="number"
              class="calculator__card-input"
              placeholder="20"
              v-model.number.trim="price"
            />
            <div class="calculator__card-error" v-if="errors.price">
              {{ errors.price }}
            </div>
          </label>
          <label class="calculator__card-label">
            <span class="calculator__card-title-input"
              >Посевная площадь, га</span
            >
            <input
              type="number"
              class="calculator__card-input"
              v-model.number.trim="square"
            />
            <div class="calculator__card-error" v-if="errors.square">
              {{ errors.square }}
            </div>
          </label>
        </div>

        <h4 class="calculator__card-profit">Прибыль от добрива</h4>
        <h4 class="calculator__card-res">{{ sum }}</h4>
        <span class="calculator__card-currency">грн</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TheCalculator",
  data() {
    return {
      sowing: 970,
      prolificness: 20,
      price: 15,
      square: 20,
      sum: this.sowing + this.prolificness + this.price + this.square,
      errors: {
        sowing: null,
        prolificness: null,
        price: null,
        square: null,
        name: null,
      },
    };
  },
  mounted() {
    this.isSum();
  },
  methods: {
    isValid() {},
    isSum() {
      this.sum =
        Number(this.sowing) +
        Number(this.prolificness) +
        Number(this.price) +
        Number(this.square);
    },
  },
  watch: {
    sowing: function () {
      console.log(this.sowing);
      this.isSum();
    },
    prolificness: function () {
      let valid = true;
      if (this.prolificness.length === 0 || this.prolificness <= 0) {
        this.errors.prolificness = "Значение не может быть меньше или равно 0";
        valid = false;
        console.log("no valid");
      } else {
        this.errors.prolificness = null;
        this.isSum();
      }
      return valid;
    },
    price: function () {
      let valid = true;
      if (this.price.length === 0 || this.price <= 0) {
        this.errors.price = "Значение не может быть меньше или равно 0";
        valid = false;
        console.log("no valid");
      } else {
        this.errors.price = null;
        this.isSum();
      }
      return valid;
    },
    square: function () {
      if (this.square.length === 0 || this.square <= 0) {
        this.errors.square = "Значение не может быть меньше или равно 0";
        console.log("no valid");
      } else {
        this.errors.square = null;
        this.isSum();
      }
    },
  },
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
  position: relative;
}
.calculator__card-title-input {
  font-family: "RobotoLight", sans-serif;
  font-weight: 90;
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
  color: $grey-low;
  padding: 0 0 0 10px;
}
.calculator__card-option {
}
.calculator__card-input {
  width: 100%;
  height: 30px;
  margin: 8px 0 0 0;
  color: $grey-low;
  padding: 10px;
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
