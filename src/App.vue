<script setup>
import { reactive, ref } from 'vue';
const activeIndex=ref(0);
const accordins=reactive([
 {
    heading:"Whats is teams ?",
    content:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci deleniti voluptatibus cupiditate quos modi quaerat, omnis aperiam cumque doloremque distinctio exercitationem architecto beatae. Inventore quis suscipit in pariatur ab et!",
    isOpen:true
 },
 
 {
    heading:"When using to Accodion Component",
    content:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci deleniti voluptatibus cupiditate quos modi quaerat, omnis aperiam cumque doloremque distinctio exercitationem architecto beatae. Inventore quis suscipit in pariatur ab et!",
    isOpen:false
 },
 {
    heading:"How can its defined ?",
    content:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci deleniti voluptatibus cupiditate quos modi quaerat, omnis aperiam cumque doloremque distinctio exercitationem architecto beatae. Inventore quis suscipit in pariatur ab et!",
    isOpen:false
 },
 {
    heading:"to do nothing ?",
    content:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci deleniti voluptatibus cupiditate quos modi quaerat, omnis aperiam cumque doloremque distinctio exercitationem architecto beatae. Inventore quis suscipit in pariatur ab et!",
    isOpen:false
 }

]) ;

</script>
 
<template>
<section class="container mx-auto flex item-center flex-col bg-slate-400 ">
    <h1 class="text-center text-5xl py-10">Event and Reactivity in vue js </h1>
    <div class="p-10 bg-gridient-to-br from-indifo-100 to-indigo-300 grid place-items-center ">
     <div class="w-6/12 mx-auto rounded border">
        <div class=" border-blue-100 text-center mb-2 shadow-lg bg-yellow-50 ">
            <h1 class=" font-medium text-gray-800  text-4xl">Servel  windows stacks on each others</h1>
            <p class="text-4xl">The accordin and control this Elements </p>
        </div>
     <div class="bg-white p-18 shadow-sm">
        
        
        <div class="h-1 w-full mx-auto border-b my-5"></div>
  
        <div  class="transti hover:bg-indigo-50" v-for="accordin in accordins">
            <!-- header -->
            <div @click="accordin.isOpen=! accordin.isOpen" class=" accordion-header cursor-pointer transition flex space-x-5 px-5 items-center text-3xl pb-6 ">
                <i class="fa fa-plus"></i>
                <h3>{{ accordin.heading }}</h3>
            </div>
            <!-- content -->
            <div class=" px-5 pt-0 text-left pb-5">
            <div class=" leading-5 font-light pl-9" v-show="accordin.isOpen">
                {{ accordin.content }}
            </div>
         </div>
        </div>

     </div>
     </div>
    </div>


    <div class="p-10 bg-gridient-to-br from-indifo-100 to-indigo-300 grid place-items-center ">
     <div class="w-6/12 mx-auto rounded border">
        <div class=" border-blue-100 text-center mb-2 shadow-lg bg-yellow-50 ">
            <h1 class=" font-medium text-gray-800  text-4xl">Servel  windows stacks on each others</h1>
            <p class="text-4xl">The accordin and control this Elements </p>
        </div>
     <div class="bg-white p-18 shadow-sm">
        
        
        <div class="h-1 w-full mx-auto border-b my-5"></div>
  
        <div  class="transti hover:bg-indigo-50" v-for="(accordin , index) in accordins">
            <!-- header -->
            <div @click="activeIndex=index" class=" accordion-header cursor-pointer transition flex space-x-5 px-5 items-center text-3xl pb-6 ">
                <i class="fa fa-plus"></i>
                <h3>{{ accordin.heading }}</h3>
            </div>
            <!-- content -->
            <div class=" px-5 pt-0 text-left pb-5" v-show="index==activeIndex">
            <div class=" leading-5 font-light pl-9" >
                {{ accordin.content }}
            </div>
         </div>
        </div>

     </div>
     </div>
    </div>

</section>
</template>
 
<style scoped>
 
</style>