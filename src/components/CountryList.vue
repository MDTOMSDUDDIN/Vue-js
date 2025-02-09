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

<table class="table table-bordered">
    <thead>
        <tr>
         <th>ID</th>
         <th>name</th>
         <th>Capital</th>
         <th>short_description</th>
         <th>flag</th>
        </tr>
    </thead>
    <tbody>
        <tr v-for="(item) in ListData">
         <td>{{ item['id'] }}</td>
         <td>{{ item['name'] }}</td>
         <td>{{ item['capital'] }}</td>
         <td>{{ item['short_description'] }}</td>
         <td><img class="w-25"  alt="flag" :src="item['flag']"></td>
        </tr>
    </tbody>
</table>

</template>
 
<style scoped>
 
</style>