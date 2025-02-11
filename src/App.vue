<script setup>
import { nextTick, onMounted, ref } from 'vue';

 const items=ref([
    'https://images.unsplash.com/photo-1738330094168-6e9728731ce8?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHwxN3x8fGVufDB8fHx8fA%3D%3D',
    'https://images.unsplash.com/photo-1736177843409-73956dc1c810?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHwyNHx8fGVufDB8fHx8fA%3D%3D',
    'https://plus.unsplash.com/premium_photo-1738566491473-713a2a865c0f?q=80&w=1972&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
 ]);
 
 let carosuel =null ;
 
 const numItems=ref('https://plus.unsplash.com/premium_photo-1669865742415-596c9a489d77?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0Mnx8fGVufDB8fHx8fA%3D%3D')

 function addNewItem(){
    items.value.push(numItems.value)
    carosuel.destroy()
    nextTick(function(){
        carosuel = new Flickity( '#carosuel', {})
    })
 }
 
 onMounted(()=>{
   carosuel = new Flickity( '#carosuel', {})
 })

</script>
 
<template>
    <div class="mb-10 text-4xl text-center">Life Cycle Hooks onMounted</div>
    <div class="mb-10 text-center space-x-6">
        <input type="text" v-model="numItems">
        <button @click="addNewItem()" class=" bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">submit </button>
    </div>
    
    <div class="mx-auto item " id="carosuel">
        <div :style="`background-image:url(${item})`" class="item" v-for="(item,index) in items" :key="item">{{ index+1 }}</div>
    </div>

</template>
 
<style scoped>
 .item{
    width: 900px;
    height: 400px;

 }
</style>