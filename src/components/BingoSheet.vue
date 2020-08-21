<template>
   <h1>It's bingo time my dudes</h1>
   <div class="sheet">
      <div class="tile" v-for="i in 12" :key="i">
         <BingoTile v-bind:text="pickTileText()"></BingoTile>
      </div>
      <div class="tile">
         <BingoTile v-bind:text="'ring_img'"></BingoTile>
      </div>
      <div class="tile" v-for="i in 12" :key="i">
         <BingoTile v-bind:text="pickTileText()"></BingoTile>
      </div>
   </div>
</template>

<script>
var allTexts = [
"1",
"2",
"3",
"4",
"5",
"6",
"7",
"8",
"9",
"10",
"11",
"12",
"13",
"14",
"15",
"16",
"17",
"18",
"19",
"20",
"21",
"22",
"23",
"24",
"25",
]

import BingoTile from './BingoTile.vue'
  export default {
    name: 'BingoSheet',
    methods: {
      pickTileText: function(){
         var randomNum = Math.floor(Math.random() * allTexts.length);
         const randomElement = allTexts[randomNum];
         allTexts.splice(randomNum, 1);
         return randomElement;
      }
    },
    components: {
     BingoTile
    },
  }
</script>

<style>
.sheet{
   display:grid;
   grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
}
.tile{
   width: 20%;
}
</style>
