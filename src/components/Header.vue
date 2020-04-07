<template>
  <header class="page-header">
    <div class="page-header__container container">
      <nav class="page-header__nav">
        <MenuList class="page-header__menu-list"></MenuList>
      </nav>
      <img src="/img/logo.svg" alt="">
      <Button text="Buy Now"></Button>
    </div>
  </header>
</template>

<script>
import MenuList from '@/components/MenuList'
import Button from '@/components/Button'
export default {
  components: {
    MenuList, Button
  }
}
</script>

<style lang="scss">
  .page-header {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
  }
  .page-header__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 18px;
    padding-bottom: 16px;
  }
</style>
