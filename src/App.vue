<template>
  <div id="app">
    <NewComponent first_name="TALIS APARECIDO DOS REIS"/>
    <NewContador />
  </div>
</template>

<script>
import NewComponent from './components/NewComponent.vue'
import NewContador from './components/NewContador.vue'

export default {
  name: 'App',
  components: {
    NewComponent,
    NewContador
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
