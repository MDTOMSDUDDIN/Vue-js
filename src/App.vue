<script setup lang="ts">
import ComponentA from './components/componentA.vue';

</script>

<template>
  <ComponentA v-slot:default="slotProps">
    <p>Name: {{ slotProps.user.name }}</p>
    <p>Age: {{ slotProps.user.age }}</p>
  </ComponentA>
</template>
