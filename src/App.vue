<template>
  <div id="app">
    <MainMenu />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MainMenu from './components/MainMenu.vue'

export default {
  name: 'app',
  components: {
    MainMenu
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
