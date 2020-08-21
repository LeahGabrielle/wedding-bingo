<template>
  <div id="app">
    <BingoSheet/>
  </div>
</template>

<script>
import BingoSheet from './components/BingoSheet.vue'

export default {
  name: 'App',
  components: {
    BingoSheet
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
