<template>
  <section class="calculator">
    <div class="calculator__card">
      <div class="calculator__card-inner">
        <h2 class="calculator__card-title">Посчитайте прибыль <br /></h2>
        <span class="calculator__card-title">добриво эфективнее химии</span>
        <label class="calculator__card-label">
          <span>Выберите культуру</span>
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
          <span>Урожайность, ц/га</span>
          <input type="text" class="calculator__card-input" />
        </label>
        <label class="calculator__card-label">
          <span>Стоимость хим. удобрения, грн/га</span>
          <input type="text" class="calculator__card-input" />
        </label>
        <label class="calculator__card-label">
          <span>Посевная площадь, га</span>
          <input type="text" class="calculator__card-input" />
        </label>
        <h4 class="calculator__card-profit">Прибыль от добрива</h4>
        <h4 class="calculator__card-res">Прибыль от добрива</h4>
        <span>грн</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TheCalculator",
};
</script>

<style lang="scss" scoped></style>
