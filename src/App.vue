<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>
    <hr> -->
    <Counter></Counter>
    <hr>
    <HoverMessage></HoverMessage>
    <hr>
    <HandlingUserInput></HandlingUserInput>
    <hr>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import Counter from './components/Counter.vue';
import HoverMessage from './components/HoverMessage.vue';
import HandlingUserInput from './components/HandlingUserInput.vue';

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Counter,
    HoverMessage,
    HandlingUserInput
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
