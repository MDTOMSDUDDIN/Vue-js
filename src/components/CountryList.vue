<script setup>
import axios from 'axios';
import { ref } from 'vue';
const ListData=ref([]);

CallCountryList();
 
async function CallCountryList(){
    let response= await axios.get("https://countrylist.teamrabbil.com/api/country-list")
    ListData.value=response.data
}

</script>
 
<template>

<p>{{ JSON.stringify(ListData) }}</p>

</template>
 
<style scoped>
 
</style>