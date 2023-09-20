<script setup>
import {computed, ref} from "vue";

const celsius = ref('');

const fahrenheit = computed(() => celsius.value*9/5+32)

</script>

<template>
  <div>
    <p>Convert from celsius to fahrenheit</p>
    <p>Fahrenheit: {{fahrenheit}}</p>
    <input v-model="celsius" placeholder="Celsius"/>
  </div>
</template>

<style scoped>

</style>
