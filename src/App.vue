<script setup>
import { ref } from 'vue';
import task from './components/task.vue';
import Radio from './components/Radio.vue';
const taskdone = ref(false);

const fruit = ref('apple');
</script>

<template>
  <div class="p-12  m-auto">
    Orginal Task:{{ taskdone }}
    <br>
    <div>
      <task label="tihs is task" v-model="taskdone" />
    </div>
  </div>



  <div class="text-center text-4xl">
    <label>Your Favarite Fruits :{{ fruit }}</label>
    <Radio v-model="fruit" label="apple" value="apple" />
    <Radio v-model="fruit" label="orange" value="orange" />
    <Radio v-model="fruit" label="banana" value="banana" />
  </div>
</template>

<style scoped></style>