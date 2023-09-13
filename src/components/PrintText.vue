<script setup>
import {ref} from "vue";

const message = ref('');
</script>

<template>
  <div>
    <p>Write some thing: {{message}}</p>
    <input v-model="message" placeholder="edit me" />
  </div>
</template>

<style scoped>

</style>