<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <X></X>
    <Y></Y>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import X from './components/X.vue'
import Y from './components/Y.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,X,Y
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
