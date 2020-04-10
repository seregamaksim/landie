<template>
  <div class="calculator-page">
    <form class="calculator" action="">
      <input class="calculator__total" type="text" value="0">
      <div class="calculator__wrap-btn">
        <button class="calculator__btn calculator__btn--clear">AC</button>
        <button class="calculator__btn calculator__btn--control">/</button>
        <button class="calculator__btn">7</button>
        <button class="calculator__btn">8</button>
        <button class="calculator__btn">9</button>
        <button class="calculator__btn calculator__btn--control">*</button>
        <button class="calculator__btn">4</button>
        <button class="calculator__btn">5</button>
        <button class="calculator__btn">6</button>
        <button class="calculator__btn calculator__btn--control">-</button>
        <button class="calculator__btn">1</button>
        <button class="calculator__btn">2</button>
        <button class="calculator__btn">3</button>
        <button class="calculator__btn calculator__btn--control">+</button>
        <button class="calculator__btn calculator__btn--zero">0</button>
        <button class="calculator__btn">.</button>
        <button class="calculator__btn calculator__btn--control">=</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: () => ({
    
  })
}
</script>

<style lang="scss">
  .calculator-page {
    min-height: 500px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .calculator__total {
    width: 100%;
    height: 60px;
    border: 0;
    background-color: #fff;
    max-width: 272px;
    text-align: right;
    font-size: 22px;
    padding: 10px;
    box-sizing: border-box;
  }
  .calculator__wrap-btn {
    display: grid;
    grid-template-columns: repeat(4, 60px);
    grid-template-rows: repeat(4, 1fr);
    grid-gap: 5px;
  }
  .calculator__btn {
    // width: 30px;
    height: 60px;
    border-radius: 50px;
    background-color: #505050;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 0;
    color: #fff;
    cursor: pointer;
    font-size: 22px;
  }
  .calculator__btn--control {
    background-color: #FF9500;
  }
  .calculator__btn--clear {
    background-color: #D4D4D2;
    color: #1C1C1C;
    grid-column: 1/4;
  }
  .calculator__btn--zero {
    grid-column: 1/3;
  }
</style>
