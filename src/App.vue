<script setup>
import { reactive, ref } from 'vue';

 
 const persons=reactive([
  {name:"tomas",age:123,email:"a@gmail.com"},
  {name:"parvax",age:21,email:"b@gmail.com"},
  {name:"rifat",age:545,email:"c@gmail.com"},
  {name:"sabbir",age:5,email:"c@gmail.com"},
 ])

 const activeIndex=ref(0)
</script>
 
<template>
 <section class="m-12 p-7 container">
  <h1 class="text-2xl mb-10">Logic Dynamic</h1>
  <p class="my-10">
    {{ persons }}
  </p>
  <div class="flex">
    <div class="w-1/2">
        <p>{{ activeIndex + 1 }}</p>
        <p class="mb-10">
            <h1>Select a person</h1>
            <select name="person" id="person" v-model="activeIndex" >
                <option :value="index" v-for="(person ,index) in persons" :key="person.name" >{{ person.name }}</option>
            </select>
        </p>
    </div>
    <div>
        <input type="text"  class="my-3" :placeholder="key" v-model="persons[activeIndex][key]" v-for="(value,key ,index2) in persons[activeIndex]" :key="key" />
    </div>
  </div>
 </section>
</template>
 
<style scoped>
 
</style>