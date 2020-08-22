<template>
   <div class="tileContainer" @click="isHidden = !isHidden">
      <p>{{text}}</p>
      <img v-if="!this.isHidden" class="dab" src="../assets/pink-circle.png"/>
   </div>
</template>

<script>
  export default {
    name: "BingoTile",
    props: ["text"],
    data: function(){
      return {
         isHidden: true
      }
   }
  }
</script>

<style>
.dab{
   height: auto;
   width: auto;
   position: absolute;
   display: block;
   max-height: 85%;
   max-width: 85%;
   transform: translate(-50%, -50%);
   top: 50%;
   left: 50%;
   opacity: 40%
}
p{
   position: absolute;
   z-index: 2;
   transform: translate(-50%, -50%);
   top: 50%;
   left: 50%;
   margin: auto;
}
.tileContainer{
   height: inherit;
   width: inherit;
}
</style>
