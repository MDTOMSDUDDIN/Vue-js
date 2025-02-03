<script setup>
import { ref } from "vue";
  const country="Bangladesh";

  const count=ref(0)
  const increment=()=>{
    count.value++;
  }
  const decrement=()=>{
    count.value--;
  }
  function incrementBy10() {
    count.value+=10;
  }

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <h1>Wellcome to Your Country: {{ country }} - {{ count }}</h1>
      <p>
        This is count: {{ count }}
      </p>
      <p>
        <button @click="increment">increment</button>
        <button @click="decrement">Decrement</button>
      </p>
      <p>
        <button @click="incrementBy10">incrementBy10</button>
      </p>
    </div>
  </header>

</template>

<style scoped>

</style>
