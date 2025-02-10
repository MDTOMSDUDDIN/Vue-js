<script setup>
import { reactive } from 'vue';

const accordins=reactive([
    false,false,false,false
]) ;

function toggle(index){
    accordins[index]= ! accordins[index];
}
</script>
 
<template>
<section class="container mx-auto flex item-center flex-col bg-slate-400 ">
    <h1 class="text-center text-5xl py-10">Event and Reactivity in vue js </h1>
    <div class="p-10 bg-gridient-to-br from-indifo-100 to-indigo-300 grid place-items-center ">
     <div class="w-6/12 mx-auto rounded border">
     <div class="bg-white p-18 shadow-sm">
        <h1 class=" font-medium text-gray-800  text-4xl">Servel  windows stacks on each others</h1>
        <p class="text-4xl">The accordin and control this Elements </p>
        <div class="h-1 w-full mx-auto border-b my-5"></div>
        
        <div  class="transti hover:bg-indigo-50 ">
            <!-- header -->
            <div @click="toggle(0)" class=" accordion-header cursor-pointer transition flex space-x-5 px-5 items-center text-3xl pb-6 ">
                <i class="fa fa-plus"></i>
                <h3>What is Teams</h3>
            </div>
            <!-- content -->
            <div class=" px-5 pt-0 text-left pb-5" v-show="accordins[0]">
            <div class=" leading-5 font-light pl-9 ">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad blanditiis placeat delectus fugit provident debitis voluptatibus quae non beatae natus! Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias, labore!
            </div>
         </div>
        </div>

        <div class="transti hover:bg-indigo-50 ">
            <!-- header -->
            <div @click="toggle(1)" class=" accordion-header cursor-pointer transition flex space-x-5 px-5 items-center text-3xl pb-6  ">
                <i class="fa fa-plus"></i>
                <h3>accordion-header part 2</h3>
            </div>
            <!-- content -->
            <div class=" px-5 pt-0 text-left pb-5" v-show="accordins[1]">
            <p class=" leading-5 font-light pl-9 ">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad blanditiis placeat delectus fugit provident debitis voluptatibus quae non beatae natus! Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias, labore!
            </p>
         </div>
        </div>

        <div class="transti hover:bg-indigo-50 ">
            <!-- header -->
            <div @click="toggle(2)" class=" accordion-header cursor-pointer transition flex space-x-5 px-5 items-center text-3xl pb-6 ">
                <i class="fa fa-plus"></i>
                <h3>accordion-header part 3</h3>
            </div>
            <!-- content -->
            <div class=" px-5 pt-0 text-left pb-5 " v-show="accordins[2]">
            <p class=" leading-5 font-light pl-9 ">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad blanditiis placeat delectus fugit provident debitis voluptatibus quae non beatae natus! Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias, labore!
            </p>
         </div>
        </div>

        <div class="transti hover:bg-indigo-50 ">
            <!-- header -->
            <div  @click="toggle(3)" class=" accordion-header cursor-pointer transition flex space-x-5 px-5 items-center text-3xl pb-6 ">
                <i class="fa fa-plus"></i>
                <h3>accordion-header part 4</h3>
            </div>
            <!-- content -->
            <div class=" px-5 pt-0 text-left pb-5 " v-show="accordins[3]">
            <p class=" leading-5 font-light pl-9 ">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad blanditiis placeat delectus fugit provident debitis voluptatibus quae non beatae natus! Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias, labore!
            </p>
         </div>
        </div>

     </div>
     </div>
    </div>

</section>
</template>
 
<style scoped>
 
</style>