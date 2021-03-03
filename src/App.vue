<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Framework</h1>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <contenu/> -->
    <contenu></contenu>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Contenu from "./components/Contenu.vue"

export default {
  name: 'App',
  components: {
    "contenu" : Contenu
    // HelloWorld
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
