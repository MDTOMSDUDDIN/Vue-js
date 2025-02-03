<script setup>
    const message="Wellcome Get Reader to master <em>Vue-Js -3</em>";
    const number =16;
    const Animal="Tiger";
    const seacrUrl="https://www.pexels.com/search/";

</script>


<template>
 <div class="container mx-auto flex items-center justify-center min-h-screen flex-col">
      <h1 class="text-4xl" v-html="message"></h1>
      <h2 class="text-xl mt-10 text-gary-700"><span> {{ number }}/4 = {{ number / 4 }} </span></h2>
      <h2 class="text-xl mt-10 text-gary-700"><span> {{ number }} is  = {{ number %2==0?"Even number":"Odd Number" }} </span></h2>
      <h2 class="text-xl mt-10 text-gary-700">
        <a target="_blank" :href="seacrUrl+Animal.toLowerCase()"> Search For {{ Animal  }}</a>
      
      </h2>
      <h2 class="text-xl mt-10 text-gary-700">
        <a target="_blank" :href="`https://www.pexels.com/search/${Animal}`"> Search For {{ Animal  }}</a>
      
      </h2>
 </div>
</template>


<style scoped>

</style>
