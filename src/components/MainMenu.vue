<template>
  <div id="main">
    <div style="box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);position: -webkit-sticky;position: sticky;top: 0;background-color: white;display: flex;padding: 5px 20px; letter-spacing: 1px;">
      <div @click="home  = true; about = doc   = team = false" style="padding: 10px; text-transform: uppercase; cursor: pointer;">Home</div>
      <div @click="about = true; home  = doc   = team = false" style="padding: 10px; text-transform: uppercase; cursor: pointer;">About</div>
      <div @click="doc   = true; home  = about = team = false" style="padding: 10px; text-transform: uppercase; cursor: pointer;">Documentation</div>
      <div @click="team  = true; home  = about = doc  = false" style="padding: 10px; text-transform: uppercase; cursor: pointer;">Team</div>
    </div>
    <template v-if="home">
      <img alt="Earth logo" src="../assets/planet-earth.png" style="margin-top:60px">
      <HelloBot msg="Welcome to Hello Bot"/>
    </template>
    <div v-if="about" style="width:300px;text-align:left;padding:10px;">
      Hello bot is a way to measure how positive or negative the sentence you are about to send. It is a great way to quickly check whether your sentence contains words that may be taken as offensive or harsh.
    </div>
    <div v-if="doc" style="width:300px;text-align:left;padding:10px;">
      Coming soon... Stay tuned!
    </div>
    <div v-if="team" style="width:300px;text-align:left;padding:10px;">
      Brandon, Cole, Jennifer, Alice
    </div>
  </div>
</template>

<script>
import HelloBot from '../components/HelloBot.vue'
export default {
  name: 'MainMenu',
  components: {
    HelloBot
  },
  data () {
    return {
      isActive: false,
      home: true,
      about: false,
      doc: false,
      team: false
    }
  }
}
</script>

<style>
#main {
  
}
</style>
