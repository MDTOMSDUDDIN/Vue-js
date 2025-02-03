<script setup>
import { ref } from 'vue';

const location="Dhaka";
const weather=ref("s")
</script>


<template>

<div class="row">
  <div class="card-header">
   <h1>Weather Map</h1>
  </div>
</div>
<h1 class="text-3xl ">{{ location }}</h1>
<h2 text-2xl v-if="weather=='s'" >Weather :Sunny</h2>
<h2 text-2xl v-if="weather=='c'" >Weather :Cloudly</h2>
<h2 text-2xl v-if="weather=='r'" >Weather :RainDay</h2>
<h2 text-2xl v-if="weather=='t'" >Weather :ThunderStrom</h2>
<img v-if="weather=='s'" src="https://cdn.pixabay.com/photo/2016/03/18/15/07/cloudiness-1265205_1280.png" alt="" class="images">
<img v-if="weather=='c'" src="https://www.svgrepo.com/show/502423/weather.svg" alt="" class="images">
<img text-2xl v-if="weather=='r'" src="https://www.svgrepo.com/show/279148/snowing-forecast.svg" alt="" class="images">
<img text-2xl v-if="weather=='t'" src="https://www.svgrepo.com/show/279158/sunrise.svg" alt="" class="images">


<input type="text" placeholder="Weather Status" class="text-center p-5" v-model="weather">
</template>


<style scoped>
.images{ 
  width: 90px;
  height: 90px;
  margin: 10px;
  padding: 5px;
}
</style>
