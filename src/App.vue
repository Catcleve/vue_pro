<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- 这里 price加上:之后，后面变成表达式，20就变成常量数字 -->
    <Car brand="宝马" :price="20" color="哈哈"></Car>
    <hr>
    <Car brand="奔驰" :price="100" ></Car>
    <hr>
    {{ count }}<button @click="test">测试，点我的话，价格会复原</button>
  </div>
</template>

<script>
import Car from './components/Car.vue'
export default {
  name: 'App',
  components: {
    Car
  },
  methods : {
    test(){
      this.count++
    }
  },
  data(){
    return{
      count : 1
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
