<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- 使用ToDo組件 -->
    <ToDo msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
//導入組件
//import HelloWorld from './components/HelloWorld.vue'
import ToDo from './components/ToDo.vue'


export default {
  name: 'app',
  //註冊組件
  components: { 
    ToDo
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
  margin-top: 60px;
}
</style>
