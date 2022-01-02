<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Titulo/>
  <Cuenta/>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Cuenta from './components/Cuenta.vue'
import Titulo from './components/Titulo.vue'


export default {
  name: 'App',
  components: {
    Cuenta,
    Titulo
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
