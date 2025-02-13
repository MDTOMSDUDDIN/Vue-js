<script setup>

 import { ref } from 'vue';
import { countries } from './data/countries';

 const search=ref('')

function getFilterCountry(){
  return countries.filter(country=>{
    return country.name.toLowerCase().startsWith(search.value.toLowerCase())
  })
}
</script>
 
<template>
 <section class=" mx-auto container m-10 p-10">
  <h1 class="text-4xl mb-10 font-bold text-center">Search Country List</h1>
  <p class="mb-4 "> {{ search }}</p>
 <p>
  Search: <input type="text" class="border" v-model="search">
 </p>
 <p>
  <ul>
    <li v-for="country in getFilterCountry()" :key="country.code">
      {{ country.name }}
    </li>
  </ul>
 </p>
 </section>
</template>
 
<style scoped>
 
</style>