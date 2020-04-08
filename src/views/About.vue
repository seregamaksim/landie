<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script>
import anime from 'animejs/lib/anime.es.js'
export default {
  mounted () {
    // eslint-disable-next-line no-unused-vars
    const tl = anime.timeline({
      easing: 'linear',
      duration: 1500
    }).add({
      targets: '.page-header',
      translateY: ['-100%', 0],
      opacity: [0, 1]
    }, 0).add({
      targets: '.about',
      translateX: [-100, 0],
      opacity: [0, 1]
    }, 0)
  },
  beforeRouteLeave (to, from, next) {
    // eslint-disable-next-line no-unused-vars
    const tl = anime.timeline({
      easing: 'linear',
      duration: 1500
    }).add({
      targets: '.page-header',
      translateY: [0, '-100%'],
      opacity: [1, 0]
    }, 0).add({
      targets: '.about',
      translateX: [0, -100],
      opacity: [1, 0]
    }, 0)
    tl.finished.then(next)
  }
}
</script>

<style lang="scss">
  .about {
    height: 500px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
