<script setup>
 const props=defineProps(['label','modelValue']);

 const emit=defineEmits(['update:modelValue']);
</script>
 
<template>
<div>
    <label for="">{{ label }}</label>
    <input type="checkbox"  :checked="modelValue" @change="$emit('update:modelValue',$event.target.checked)">
</div>
</template>
 
<style scoped>
 
</style>