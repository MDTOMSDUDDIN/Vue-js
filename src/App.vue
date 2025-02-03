<script setup>
import AlertComponents from './components/AlertComponents.vue';

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
    
    <AlertComponents type="error"  msg="hello world"/><br>

    <alert-components type="success" msg="success" /><br>
    <alert-components type="warning"/>
    <alert-components />
      
    </div>
  </header>

</template>

<style scoped>

</style>
