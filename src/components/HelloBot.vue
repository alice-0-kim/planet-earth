<template>
  <div class="hello" style="min-height:1000px;">
    <h1>{{ msg }}</h1>
    <input v-model="phrase" class="input" style="width:350px;">
    <button @click="rephrase(phrase)" type="submit" class="button success animate">Submit</button>
    <div v-html="response">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloBot',
  props: {
    msg: String
  },
  data () {
    return {
      phrase: '',
      response: ''
    }
  },
  methods: {
    rephrase (phrase) {
      var Sentiment = require('sentiment');
      var sentiment = new Sentiment();
      var result = sentiment.analyze(phrase);

      const response = result.score >= 0 ?
        'Looks great! Keep up with your positivity!' :
        `Hmm... <span style="color:red">${result.negative.toString()}</span> worries me. Is everything alright?`
      this.response = response;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.animate {
  transition: all ease 0.3s;
}
.input {
  border: none;
  box-shadow: 1px 1px 1px 1px rgba(0,0,0,0.2);
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: medium;
  height: 35px;
  margin: 0 20px 20px 0;
  padding: 0 10px;
}
.input:focus, .button:focus {
  outline: none;
}
.button {
  border: none;
  border-radius: 5px;
  box-shadow: 1px 1px 1px 1px rgba(0,0,0,0.2);
  letter-spacing: 1px;
  text-transform: uppercase;
  padding: 10px 15px;
  cursor: pointer;
}
</style>
