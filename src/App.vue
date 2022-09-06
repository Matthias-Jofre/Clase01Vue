<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <MyCounter @selection="checkAnswer"></MyCounter>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MyCounter from './components/MyCounter.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    MyCounter
},
methods: {
    checkAnswer(num) {
      console.log((num))
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
}
</style>
