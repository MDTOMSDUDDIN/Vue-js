<script setup>
import { ref } from 'vue';

 
  const multibox=ref([])
</script>
 
<template>
<h1 class="text-2xl mb-3 text-center">Vue from</h1>
<div class="text-2xl mb-3 text-center ">
   <p class="text-2xl mb-10 text-center ">{{ multibox }}</p>
   <label >red</label>
   <input type="checkbox" v-model="multibox" value="red" class="ml-2 mr-2" />
   <label>green</label>
   <input type="checkbox" v-model="multibox" value="green" class="ml-2 mr-2" />
   <label>blue</label>
   <input type="checkbox" v-model="multibox" value="blue" class="ml-2 mr-2" />
</div>
</template>
 
<style scoped>
 
</style>