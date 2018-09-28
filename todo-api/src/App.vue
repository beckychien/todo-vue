<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- 使用ToDo、Test組件 -->
    <!-- <HeaderView msg="父組件傳值給子組件"></HeaderView> -->
    
    <HeaderView :msg="title"></HeaderView>
    <!-- 觸發ToDo子組件中的myMsg事件（將子組件的值傳遞給父組件）並調用getData方法 -->
    <ToDo @myMsg='getData'></ToDo>
    
  </div>
</template>

<script>
//導入組件
//import HelloWorld from './components/HelloWorld.vue'
import ToDo from './components/ToDo.vue'
import HeaderView from './components/Header.vue'

//app.vue是父組件,Todo、Header是子組件
//父->子：props
//子->父：自定義事件

export default {
  name: 'app',
  //註冊組件
  components: { 
    ToDo,HeaderView
  },
  Data(){
    return {
      title: "Data中的標題"
    }
  },
  methods:{
    getData(msg){
      console.log("App.Vue:"+msg);
      this.title=msg;
    }
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
