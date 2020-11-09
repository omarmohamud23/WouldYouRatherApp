<template>
  <div id="app">
    
 <h1>Would you rather...?</h1>

<would-you-rather  v-bind:question="wyrQuestion"
 v-bind:answer1="wyrAnswer1"
 v-bind:answer2="wyrAnswer2" v-on:answer-changed="answerChanged"></would-you-rather>



 <p>{{ userSelectionMessage }}</p>
 
 
 
  </div>
</template>

<script>
import WouldYouRather from './components/WouldYouRather.vue'

export default {
  name: 'App',
  components: {
    WouldYouRather
  },
  data(){
    return{
      wyrQuestion:' Would you rather be a wizard or a superhero?',
      wyrAnswer1:'Wizard',
      wyrAnswer2:'Superhero',
      userSelectionMessage: ''
    }
  },
  methods: {
    answerChanged(choice)  {
      this.userSelectionMessage = `Thanks! You chose ${choice}`
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background: bisque;
}
</style>
