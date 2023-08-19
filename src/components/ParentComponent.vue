<script setup>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

const messageFromParent = 'Hello my child from Parent Component';
let emittedMessage = ref('');

const handleMessageEmitted = (message) => {
  emittedMessage.value = message;
};

</script>

<template>
    <div>
        <ChildComponent :message="messageFromParent" @messageEmitted="handleMessageEmitted" />
        <p>Message from ChildComponent: {{ emittedMessage }}</p>
  </div>
</template>

<style scoped>

</style>

