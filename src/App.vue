<script setup>
import { reactive } from 'vue';

 const saarsCountries=reactive([
  {name:'bangladesh', capital:'Dhaka'},
   {name:'Canada', capital:'Ottawa'},
  {name:'Brazil', capital:'Brasília'},
  {name:'Japan', capital:'Tokyo'},
  {name:'Australia', capital:'Canberra'},
  {name:'South Africa', capital:'Pretoria'}
 ])
 const capitals=["Dhaka","Ottawa","Brasília","Tokyo","Canberra","Pretoria"]

 function getRandomCapitials(){
  // return capitals.sort(()=>Math.random() -0.5)
  return capitals
 }

 function getscore(){
  let Score=0;
  saarsCountries.forEach(country=>{
    if(country.answer===country.capital){
      Score++
    }
  })
  return Score
 }
</script>
 
<template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10 text-center">Vuejs Simple Quiz projects</h1>
    <p class="mb-10">{{ saarsCountries }}</p>
    <p class="mb-10 text-center">Total Score : {{ getscore() }}</p>
    <div class="my-5 m-5 p-4 border border-gray-500" v-for="(country,index) in saarsCountries" :key="country.name" >
      <p class="mb-1">Whats is the Capital of {{ country.name }} ?</p>
      <template v-for="capital in getRandomCapitials()">
      <input :name="country.name" type="radio" :value="capital"  v-model="country.answer">
      <label for="" class="ml-2 mr-2">{{capital }}</label>
      </template>
    </div>
  </section>
</template>
 
<style scoped>
 
</style>