<template>
  <ul class="menu">
    <router-link v-for="link in links" class="menu__item" :key="link.url" tag="li" :to="link.url">
      <a href="#" class="menu__link">{{link.title}}</a>
    </router-link>
  </ul>
</template>

<script>
export default {
  data: () => ({
    links: [
      { title: 'Home', url: '/' },
      { title: 'About', url: '/about' },
      { title: 'Contact', url: '/contact' }
    ]
  })
}
</script>

<style lang="scss">
  .menu {
    display: flex;
    width: 100%;
    max-width: 245px;
    margin: 0;
    padding: 0;
  }
  .menu__item {
    min-width: 65px;
    margin-right: 30px;
    list-style: none;
  }
  .menu__item:last-child {
    margin-right: 0;
  }
  .menu__link {
    font-size: 14px;
    line-height: 24px;
    color: #505F98;
    text-decoration: none;
  }
</style>
