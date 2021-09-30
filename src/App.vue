<template>
  <div id="app">
    <cabecera titulo= "Menu"></cabecera>
    <cuerpo></cuerpo>
    <pie autor= "Camila Beczkowski y Natanel Gutkind"></pie>
  </div>
</template>

<script>


import Pie from './components/Pie.vue'
import Cabecera from './components/Cabecera.vue'
import Cuerpo from './components/Cuerpo.vue'

export default {
  name: 'App',
  components: {
    Cabecera,
    Pie,
    Cuerpo,
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
