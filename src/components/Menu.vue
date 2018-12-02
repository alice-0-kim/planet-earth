<template>
  <div id="main" style="box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);position: -webkit-sticky;position: sticky;top: 0;background-color: white;display: flex;padding: 5px 20px; letter-spacing: 1px;">
      <div style="padding: 10px; text-transform: uppercase; cursor: pointer;">About</div>
      <div style="padding: 10px; text-transform: uppercase; cursor: pointer;">Documentation</div>
      <div style="padding: 10px; text-transform: uppercase; cursor: pointer;">Team</div>
  </div>
</template>

<script>
export default {
  name: 'MainMenu'
}
</script>

<style>
#main {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
