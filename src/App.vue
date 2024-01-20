<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Card 
  foto="https://cdni.fancaps.net/file/fancaps-animeimages/13785769.jpg" 
  msg="Это картинка терминатора!!!!" />
 
  <Card 
  foto="https://w.forfun.com/fetch/55/55b3a38aa5064e0a9061f9a9198d4e6f.jpeg"
  msg="jbhcvbwubwiuvbibv" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Card
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
