<script setup>
const bgOrange=" bg-orange-400";
const bgindigo=" bg-indigo-400";
const bggreen=" bg-green-400";

const weekday=true;

const colors={
    bgColor:"bg-teal-100",
    borderColor:"border-teal-500",
    textColor:"text-teal-900",
}

const messageType='warning';

if('error'==messageType){
    colors.bgColor='bg-red-100',
    colors.borderColor='border-red-500',
    colors.textColor='text-red-900'
}
else if('success'==messageType){
    colors.bgColor='bg-green-100',
    colors.borderColor='border-green-500',
    colors.textColor='text-green-900'
}
else if('warning'==messageType){
    colors.bgColor='bg-orange-100',
    colors.borderColor='green-orange-500',
    colors.textColor='text-orange-900'
}

</script>

<template>
    <section class="container mx-auto">
        <h4 class="text-center py-12 text-3xl">Class & Style binding</h4>

        <section class="flex space-x-10">
        <div class="w-1/3 h-16" :class="bgOrange" ></div>
        <div class="w-1/3 h-16" :class="bgindigo" ></div>
        <div class="w-1/3 h-16" :class="bggreen"></div>
        </section>
    
        <section class="mt-10 ">
            <div class=" h-16 flex items-center justify-center text-white" :class="[weekday?'bg-red-600':'bg-green-600', weekday==true?'text-2xl':'text-4xl']">
                Its is a Weekday !
            </div>
        </section>

        <section class="mt-10 ">
            <div class=" border-t-4 rounded-b py-3 shadow-md" :class="[colors.bgColor,colors.borderColor,colors.textColor]">
                <p class="font-blod">Our Privicy Policy Has Changed</p>
                <p class="text-sm">Make sure you Know how these change Effet</p>
            </div>
        </section>
    </section>
</template>

<style scoped>

</style>
