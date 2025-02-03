<script setup>
// const type="error";
// const msg="this is an message !";
// defineProps(['type','msg']);
   
 defineProps({
   type:{
    type:String,
    default:'info',
   },
   msg:{
    type:String,
    default:"this is alert message ",
   }
 });

const GetColors=(type)=>{
  const colors={
    'info':'bg-blue-100 text-blue-800',
    'success':'bg-green-100 text-green-800',
    'error':'bg-red-100 text-red-800',
    'warning':'bg-yellow-100 text-yellow-800',
  }
  return colors[type] || colors['info'];
}
</script>

<template>
<div class="p-4 mb-4 text-sm  rounded-lg " :class="GetColors(type)" role="alert">
  <span class="font-medium">{{ msg }}</span>
</div>
</template>

<style scoped>

</style>