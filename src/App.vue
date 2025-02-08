<script setup>
function onformsubmit(){
  alert('form submit successfull ')
}
function onClick(){
  alert('i am click event');
}

function OnRightClick(){
  alert('on right click Event ');
}

function OnLeftClick(){
  alert('on left click event ');
}
function onChange(){
  alert('I am On Change Event');
}
</script>

<template>
  <form @submit.prevent="onformsubmit">
    <button type="submit">Form submit Event </button>
  </form>


  <button @click="onClick">Click event </button>
  
  <button @click.right="OnRightClick">Right click Event</button>
  <button @click.left="OnLeftClick">left click Event</button>
  <input @change="onChange" placeholder="On change Event ">
  <input @keyup="onChange" placeholder="On keyup ">
  <input @keydown="onChange" placeholder="On keydown Event ">
</template>

<style scoped>

</style>
