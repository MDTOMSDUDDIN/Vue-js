<script setup>
import { ref } from 'vue';
import TextComponent from './components/TextComponent.vue';

const name = ref('tomas uddin');
const email = ref('t@gmail.com');
</script>

<template>
  <div class="p-12  m-auto">
    Orginal Name:{{ name }} <br>
    Orginal email:{{ email }}
    <br>
    <div>
      <label for="">Name :</label>
      <input type="text" v-model="name">
    </div>
    <br><br>
    <div>
      <label for="">Component Value:</label><br><br>
      <TextComponent label="name" v-model="name" />
      <TextComponent label="email" v-model="email" />
    </div>
  </div>
</template>

<style scoped></style>