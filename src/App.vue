<template>
  <div id="app">
    <exportandoComponente/>

  </div>
</template>

<script>
import exportandoComponente from './components/exportandoComponente.vue'

export default {
  name: 'App',
  components: {
    exportandoComponente
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
