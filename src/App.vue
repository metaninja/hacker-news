<template>
  <main id="app" class="page-container">
    <app-bar-top></app-bar-top>
    <new-articles></new-articles>
  </main>
</template>

<script>
import News from './components/News.vue';
import AppBarTop from './components/AppBarTop.vue';


export default {
  name: 'app',
  components: {
      'app-bar-top': AppBarTop,
      'new-articles': News
  }
}
</script>

<style>
#app {
  font-family: 'Roboto', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
