<script setup>
const bgOrange='background-color:red';
const bgindigo='background-color:green';
const bggreen='background-color:orange';

const bgRed='background-color:red';
const bgDarkGreen='background-color:green';


const weekday=true;

const colors={
    backgroundColor:"info",
    borderColor:"info",
   color:'white',
}
const messageType='success';

if('error'==messageType){
    colors.backgroundColor='red',
    colors.borderColor='red',
    colors.color='white'
}
else if('success'==messageType){
    colors.backgroundColor='green',
    colors.borderColor='darkgreen',
    colors.color='white'
}
else if('warning'==messageType){
    colors.backgroundColor='orange',
    colors.borderColor='orange',
    colors.color='white'
}

</script>

<template>
    <section class="container mx-auto">
        <h4 class="text-center py-12 text-3xl">Class & Style binding</h4>

        <section class="flex space-x-10">
        <div class="w-1/3 h-16" :style="bgOrange" ></div>
        <div class="w-1/3 h-16" :style="bgindigo"></div>
        <div class="w-1/3 h-16" :style="bggreen"></div>
        </section>
    
        <section class="mt-10 ">
            <div class=" h-16 flex items-center justify-center text-white" :style="[weekday?bgRed:bgDarkGreen, weekday==true?'text-2xl':'text-4xl']">
                Its is a Weekday !
            </div>
        </section>

        <section class="mt-10 ">
            <div class=" border-t-4 rounded-b py-3 shadow-md" :style="colors">
                <p class="font-blod">Our Privicy Policy Has Changed</p>
                <p class="text-sm">Make sure you Know how these change Effet</p>
            </div>
        </section>
    </section>
</template>

<style scoped>

</style>
