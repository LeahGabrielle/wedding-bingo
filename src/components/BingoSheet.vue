<template>
   <h1>It's bingo time my dudes</h1>
   <div v-for="i in 4" :key="i">
      <BingoTile v-bind:text="pickTileText()"></BingoTile>
   </div>
</template>

<script>
var allTexts = [
"1",
"2",
"3"
]

import BingoTile from './BingoTile.vue'
  export default {
    name: 'BingoSheet',
    methods: {
      pickTileText: function(){
         var randomNum = Math.floor(Math.random() * allTexts.length);
         const randomElement = allTexts[randomNum];
         allTexts.splice(randomNum, 1);
         //console.log(allTexts);
         return randomElement;
      }
    },
    components: {
     BingoTile
    },
  }
</script>

<style>

</style>
