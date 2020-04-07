<template>
  <button class="btn">
    {{text}}
  </button>
</template>
<script>
export default {
  props: {
    text: String
  }
}
</script>

<style lang="scss">
  .btn {
    font-weight: 500;
    font-size: 12px;
    line-height: 18px;
    color: #fff;
    text-align: center;
    background-color: #111B47;
    min-width: 160px;
    border: 0;
    border-radius: 2px;
    min-height: 26px;
    box-sizing: border-box;
    padding-left: 10px;
    padding-right: 10px;
  }
</style>
