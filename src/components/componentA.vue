<script setup>
import { inject } from 'vue';

const person = inject('person'); 
</script>

<template>
  <div>
    <h2>Name: {{ person.name }}</h2>
    <h3>Address: {{ person.address }}</h3>
  </div>
</template>
