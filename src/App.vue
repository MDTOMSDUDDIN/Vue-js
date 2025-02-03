<script setup>
import { ref } from "vue";
const time="mornig";

const Countries=ref([
  {name:'Bangladesh', capital:'Dhaka'},
  {name:'Bangladesh', capital:'Dhaka'},
  {name:'Bangladesh', capital:'Dhaka'},
  {name:'Bangladesh', capital:'Dhaka'},
]);



</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
     <h1 v-if="time=='morning'">Good Morning </h1>
     <h1 v-else-if="time=='afternoon'">Good Afternoon </h1>
     <h1 v-else>Good Evening</h1>


     <h1>Countries With Capitals :</h1>
     <ul>
      <li v-for="country in Countries" :key="country.name">
        {{ country.name }} - {{ country.capital }}
      </li>
     </ul>
     <ul>
      <li v-for="country, index in Countries">
       {{ index+1 }} {{ country.name }} - {{ country.capital }}
      </li>
     </ul>
    
    </div>
  </header>

</template>

<style scoped>

</style>
