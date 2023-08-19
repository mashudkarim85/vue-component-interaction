<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  message: String,
});
const emit  = defineEmits();
  
const emitMessage = () => {
    emit('messageEmitted', 'Custom message from Child Component');
};
</script>


<template>
    <div>
      <p>Message from ParentComponent: {{ props.message }}</p>
      <button class="bg-red-500 my-5 text-white" @click="emitMessage">Emit Message</button>
    </div>
  </template>
  

  
