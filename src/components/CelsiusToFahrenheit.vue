<script setup>
import {ref} from "vue";

const celsius = ref('');

</script>

<template>
  <div>
    <p>Convert from celsius to fahrenheit</p>
    <p>Fahrenheit: {{celsius*9/5+32}}</p>
    <input v-model="celsius" placeholder="Celsius"/>

  </div>
</template>

<style scoped>

</style>
