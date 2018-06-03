<template>
  <div id="app">
    <News></News>
  </div>
</template>

<script>
import News from './components/News.vue';

export default {
  name: 'app',
  components: {
    News
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
