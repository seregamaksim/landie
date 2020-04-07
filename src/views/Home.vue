<template>
  <div class="home">
    <section class="home__first-block first-block">
      <div class="container first-block__container">
        <div class="first-block__description">
          <h2 class="first-block__title">Introduce Your Product Quickly & Effectively</h2>
          <p class="first-block__text">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.</p>
          <div class="first-block__button-wrap">
            <Button class="first-block__ui-btn" text="Purchase UI Kit"></Button>
            <router-link class="first-block__more-link" to="/">Learn More</router-link>
          </div>
        </div>
        <img class="first-block__img" src="/img/head-img.svg" alt="">
      </div>
    </section>
    <section class="second-section">
      <div class="second-section__container container">
        <div class="text-block">
          <h3 class="text-block__title">Light, Fast & Powerful</h3>
          <p class="text-block__text">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.</p>
          <ul class="text-block__list">
            <li class="text-block__item">
              <img class="text-block__item-img" src="/img/text-icon.svg" alt="">
              <h4 class="text-block__item-title">Title Goes Here</h4>
              <p class="text-block__item-text">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. </p>
            </li>
            <li class="text-block__item">
              <img class="text-block__item-img" src="/img/text-icon.svg" alt="">
              <h4 class="text-block__item-title">Title Goes Here</h4>
              <p class="text-block__item-text">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. </p>
            </li>
          </ul>
        </div>
        <img src="/img/text-block-img.svg" alt="">
      </div>
    </section>
    <section>
      <div class="container">
        <ul>
          <AdvantagesItem urlImg="/img/advantages1.svg" title="Light, Fast & Powerful" text="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim."></AdvantagesItem>
          <AdvantagesItem urlImg="/img/advantages2.svg" title="Light, Fast & Powerful" text="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim."></AdvantagesItem>
          <AdvantagesItem btn urlImg="/img/advantages3.svg" title="Light, Fast & Powerful" text="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim."></AdvantagesItem>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Button from '@/components/Button'
import AdvantagesItem from '@/components/AdvantagesItem'
export default {
  name: 'Home',
  data: () => ({
    items: [
      { id: 1, url: '/img/advantages1.svg', title: 'Test', text: 'test' },
      { id: 2, url: '/img/advantages2.svg', title: 'Test', text: 'test' },
      { id: 3, url: '/img/advantages3.svg', title: 'Test', text: 'test' }
    ]
  }),
  components: {
    Button, AdvantagesItem
  }
}
</script>

<style lang="scss">
  @import '/node_modules/normalize.css';
  .first-block {
    display: flex;
    overflow: hidden;
    padding-top: 300px;
    background: url('/img/volna.svg') no-repeat;
    // background-size: contain;
    background-position: -210% center;
    margin-bottom: 110px;
  }
  .first-block__title {
    font-size: 50px;
    line-height: 66px;
    font-weight: 500;
    letter-spacing: 1px;
    color: #091133;
    margin-bottom: 20px;
  }
  .first-block__text {
    font-size: 18px;
    line-height: 30px;
    color: #505F98;
    margin-bottom: 69px;
  }
  .first-block__img {
    margin-right: -45%;
  }
  .first-block__button-wrap {
    display: flex;
  }
  .first-block__description {
    width: 100%;
    max-width: 540px;
  }
  .first-block__container {
    display: flex;
    justify-content: space-between;
  }
  .first-block__ui-btn {
    margin-right: 30px;
    min-width: 189px;
  }
  .first-block__more-link {
    min-height: 36px;
    min-width: 189px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 2px solid #091133;
    color: #091133;
    background-color: transparent;
    text-decoration: none;
    font-weight: 500;
    font-size: 16px;
    line-height: 26px;
  }
  .second-section {
    margin-bottom: 110px;
  }
  .second-section__container {
    display: flex;
  }
  .text-block {
    align-self: center;
  }
  .text-block__list {
    display: flex;
  }
  .text-block__item {
    list-style: none;
  }
  .text-block__title {
    font-size: 36px;
    line-height: 48px;
    margin-bottom: 12px;
    color: #091133;
  }
  .text-block__text {
    font-size: 16px;
    line-height: 26px;
    margin-bottom: 100px;
    color: #6F7CB2;
  }
  .text-block__item-title {
    font-size: 16px;
    line-height: 26px;
    color: #091133;
    margin-bottom: 10px;
  }
  .text-block__item-text {
    font-size: 12px;
    line-height: 18px;
  }
</style>
