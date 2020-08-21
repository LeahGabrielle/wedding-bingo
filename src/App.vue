<template>
  <div id="app">
  <h1>Virtual Bachelorette Bingo</h1>
  <h2>Have a drink when...</h2>
    <BingoSheet/>
    <h2>finish your drink when you finish a row!</h2>
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
