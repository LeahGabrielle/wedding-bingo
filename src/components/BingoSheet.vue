<template>
   <div class="sheet">
      <div class="tile" v-for="i in 12" :key="i">
         <BingoTile v-bind:text="pickTileText()"></BingoTile>
      </div>
      <div class="tile ring">
         <BingoTile v-bind:text="'text'"></BingoTile>
      </div>
      <div class="tile" v-for="i in 12" :key="i">
         <BingoTile v-bind:text="pickTileText()"></BingoTile>
      </div>
   </div>
</template>

<script>
var allTexts = [
"Someone's screen freezes",
"Eric is mentioned",
"\"Same penis forever\"",
"\"I think you're muted\"",
"Someone takes a pic for social media",
"Megan finishes her drink",
"A pet joins the call",
"Someone suggests shots",
"Someone mentions the wedding night",
"Someone has wifi problems",
"\"Are you nervous\"",
"Someone opens a new bottle of wine",
"An embarrassing tale about Megan is told",
"Someone gets emotional",
"Megan happy cries",
"Dancing happens",
"There's an awkward silence",
"Sexual innuendos are said",
"Someone has to pee",
"Shots are taken",
"Someone takes a call",
"\"Unprecedented times\"",
"Someone wears a mask",
"Someone has to go to bed",
"Megan models her new underpants",
"A male enters the room",
"Someone has to call ralph on the big white telephone",
"A doorbell rings",
"Covid-19 is mentioned",
"The honeymoon is mentioned",
"Everyone talks at once",
"\"Awww\"",
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
   padding: 0 5%;
}
.tile{
   border: 1px solid black;
   height: 200px;
   position: relative;

}
body{
  background-image: url("../assets/pink-sparkles.gif");
}
.ring{
   background-image: url("../assets/ring.png");
   background-size: contain;
   background-repeat: no-repeat;
   background-position: center;

}
.ring p {
   display:none;
}
</style>
