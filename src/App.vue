<script setup>
import { ref } from 'vue';

 const FullName=ref('https://images.pexels.com/photos/30650072/pexels-photo-30650072/free-photo-of-modern-minimalist-living-room-interior-design.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2')
 const images=[
   {
      fullName:"https://images.pexels.com/photos/30650072/pexels-photo-30650072/free-photo-of-modern-minimalist-living-room-interior-design.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
      Thumbnail:"https://images.pexels.com/photos/30650072/pexels-photo-30650072/free-photo-of-modern-minimalist-living-room-interior-design.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
   },
   
   {
      fullName:"https://images.pexels.com/photos/13938350/pexels-photo-13938350.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
      Thumbnail:"https://images.pexels.com/photos/13938350/pexels-photo-13938350.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
   },
   {
      fullName:"https://images.pexels.com/photos/28549672/pexels-photo-28549672/free-photo-of-minimalist-interior-with-shadows-in-kyiv.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load",
      Thumbnail:"https://images.pexels.com/photos/28549672/pexels-photo-28549672/free-photo-of-minimalist-interior-with-shadows-in-kyiv.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load"
   },
 
   {
      fullName:"http://images.pexels.com/photos/30635845/pexels-photo-30635845/free-photo-of-elegant-hand-holding-a-single-pink-tulip-flower.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load",
      Thumbnail:"http://images.pexels.com/photos/30635845/pexels-photo-30635845/free-photo-of-elegant-hand-holding-a-single-pink-tulip-flower.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load"
   },
 ]

 function SetImage(image){
   FullName.value=image.fullName
 }
</script>
 
<template>
<section class=" container mx-auto flex flex-col">
   <h1 class=" text-4xl text-center m-3 p-3">Event & Reactivity</h1> 
   <div class="">
      <div class="flex justify-center items-center space-x-2">
         <img @click="SetImage(image)" class=" cursor-pointer h-[300px] w-1/6" v-for="image in images" :src="image.Thumbnail">
      </div>
      <h1  class="text-4xl m-=3 text-center bg-indigo-50">Show Carousel</h1>
      <div class="mt-5 flex justify-center  items-center ">
        
         <img class=" cursor-pointer min-h-1.5 flex " :src="FullName">
      </div>
   </div>
    
</section>
</template>
 
<style scoped>
 
</style>