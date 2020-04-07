<template>
  <div id="app">
    <Header></Header>
    <transition mode="in-out" appear="">
      <router-view/>
    </transition>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'
export default {
  components: {
    Header, Footer
  }
}
</script>
<style>
body,html,p,h1,h2,h3,button,ul {
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Roboto', sans-serif;
}
#app {
  position: relative;
}
.container {
  max-width: 1110px;
  margin: 0 auto;
}
</style>
