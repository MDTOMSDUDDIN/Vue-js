<script setup>
import { ref } from 'vue';


const massage=ref("Hello VueJs -3")
const space =ref(0)

function spacePress(){
   space.value++
   massage.value="Space Pressed " + space.value+" Times"
}

function keyPress(event){
   massage.value="Key Press : "+ event.key
}

function submitPrevent(){
   massage.value="Click a submit button";
}
function ctrlRightClick(){
   massage.value="Ctrl + Right Click";
}

function DivClicked(){
   alert("Div Clicked")
}
function ButtonClick(){
   alert("Button Clicked")
}
</script>
 
<template>
<section class=" container mx-auto  items-center flex flex-col">
   <h1 class=" text-4xl text-center m-3 p-3">Event & Reactivity in Vue js </h1> 
   <div class="mt-10">{{ massage }}</div>
   <form @submit.prevent action="https://google.com/search">
      <div class="container mx-auto flex space-x-5 justify-center m-5">
         <input @keyup.space="spacePress()" type="text" name="q" class="border border-gray-500 bg-white p-5 " placeholder="Press space">
      </div>
      
      <div class="container mx-auto flex space-x-5 justify-center m-5">
         <input @keyup="keyPress($event)" type="text" name="q" class="border border-gray-500 bg-white p-5 " placeholder="Typing Somethings">
      </div>
      <button @click.prevent="submitPrevent()" class=" bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
         Button
      </button>

      
      <button @click.ctrl.right="ctrlRightClick()" class=" bg-blue-500 ml-5 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Ctrl + Right Click
      </button>
   </form>

   <div @click="DivClicked()" class="bg-gray-200 w-[500px] h-80 mt-5 flex justify-center items-center">
      <button @click.stop="ButtonClick()" class=" bg-orange-500 hover:bg-orange-700 text-white font-bold py-2 px-4 rounded">
         Button
      </button>
   </div>
</section>
</template>
 
<style scoped>
 
</style> 