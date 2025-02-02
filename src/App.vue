<script setup>
const message="Wellcome Get Reader to master Vue-Js -3";
const date="12 jan 2025";

function GetDate(){
  const  date=new Date()
  return date.toDateString()
}

</script>


<template>
    <div class="container mx-auto flex items-center justify-center min-h-screen flex-col">
      <h1 class="text-4xl">{{ message }}</h1>
      <h2 class="text-xl mt-10 text-gary-700">Todoy is <span>{{ GetDate() }}</span></h2>

    </div>
</template>


<style scoped>

</style>
