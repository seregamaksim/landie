<template>
  <footer class="page-footer">
    <div class="page-footer__container container">
      <div class="page-footer__top">
        <p class="page-footer__copyright">©2019 UIX</p>
        <router-link to="/"><img src="/img/logo.svg" alt=""></router-link>
        <Button text="Footer btn"></Button>
      </div>
      <div class="page-footer__bottom">
        <ul class="page-footer__menu">
          <li class="page-footer__menu-item"><router-link to="/">Home</router-link></li>
          <li class="page-footer__menu-item"><router-link to="/about">About</router-link></li>
          <li class="page-footer__menu-item"><router-link to="/contact">Contact</router-link></li>
        </ul>
        <ul class="page-footer__social-list">
          <li class="page-footer__social-item"><router-link to="#"><img src="/img/fb.svg" alt=""></router-link></li>
          <li class="page-footer__social-item"><router-link to="#"><img src="/img/in.svg" alt=""></router-link></li>
          <li class="page-footer__social-item"><router-link to="#"><img src="/img/tw.svg" alt=""></router-link></li>
          <li class="page-footer__social-item"><router-link to="#"><img src="/img/yt.svg" alt=""></router-link></li>
          <li class="page-footer__social-item"><router-link to="#"><img src="/img/inst.svg" alt=""></router-link></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
import Button from './Button'

export default {
  components: {
    Button
  }
}
</script>

<style lang="scss">
  .page-footer {
    background-color: #E7ECFF;
    padding-top: 65px;
    padding-bottom: 32px;
  }
  .page-footer__top,
  .page-footer__bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .page-footer__top {
    padding-bottom: 40px;
    border-bottom: 1px solid #CDD1D4;
  }
  .page-footer__bottom {
    padding-top: 20px;
  }
  .page-footer__copyright {
    font-size: 14px;
    line-height: 24px;
    color: #929ECC;
  }
  .page-footer__menu,
  .page-footer__social-list {
    display: flex;
    list-style: none;
  }
  .page-footer__menu-item {
    margin-right: 60px;
  }
  .page-footer__menu-item:last-child {
    margin-right: 0;
  }
  .page-footer__menu-item a {
    font-size: 14px;
    line-height: 24px;
    color: #929ECC;
    text-decoration: none;
  }
  .page-footer__social-item {
    margin-right: 30px;
  }
  .page-footer__social-item:last-child {
    margin-right: 0;
  }
</style>
