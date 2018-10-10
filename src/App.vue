<template>
  <div id="app">
    <img src="./assets/logo.png">
    <userscomponent></userscomponent>
  </div>
</template>

<script>

import prueba from './components/Test'
import userscomponent from './components/Users'

export default {
  name: 'App',
  components: {
    prueba,userscomponent
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
