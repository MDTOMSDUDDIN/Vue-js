<script setup>
import { reactive } from 'vue';


const myFormData=reactive({
    user:"",
    password:"",
})
function formdata(){
    console.log(myFormData);
}
</script>

<template>
  <form @submit.prevent="formdata" >
    <label >User Name =>{{ myFormData.user }}</label><br>
    <input v-model="myFormData.user" type="text" placeholder="User Name"><br>

    
    <label >Password=>{{ myFormData.password }}</label><br>
    <input v-model="myFormData.password" type="possword" placeholder="Password"><br>

    <button type="submit">submit</button>

  </form>
</template>

<style scoped>

</style>
