<script setup>
import { provide, reactive } from 'vue';
import ComponentA from './components/componentA.vue';
const person=reactive({
  name:'tomas',
  address:'sirajgonj',
});
provide('person',person); 

</script>
 
<template>
<ComponentA />
</template>
 
<style scoped>
 
</style>