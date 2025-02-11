<script setup>
import { onBeforeMount, onMounted, ref } from 'vue';

const status=ref([])
const apiResponse=ref(null)
onBeforeMount(()=>{
   console.log("Before Mount ")
   status.value.push("Before Mount")

   fetch('https://jsonplaceholder.typicode.com/todos/2')
   .then(Response=>Response.json())
   .then(json=>{
      apiResponse.value=json
   })
})

onMounted(()=>{
   console.log(" Mounted ")
   status.value.push("Mounted")
})
</script>
 
<template>
<section class=" container mx-auto  items-center flex flex-col">
   <h1 class=" text-4xl text-center m-3 p-3">Life cycle Hooks</h1> 
   <hr class="border-t border-red-500  w-full">
  <div class=" flex justify-between mt-20">
   <div class="w-1/2">
      <img  src="https://vuejs.org/assets/lifecycle.MuZLBFAS.png" alt="">
   </div>
   <div class="text-2xl w-1/2">
      {{ status }}
   </div>
   <p>{{ apiResponse }}</p>
  </div>


 
</section>
</template>
 
<style scoped>
 
</style> 