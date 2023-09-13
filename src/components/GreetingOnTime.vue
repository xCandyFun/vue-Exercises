<script setup>
const date = new Date();
const time = date.getHours();
</script>

<template>
  <div>
    <h1 v-if="time<12">Good morning</h1>
    <h1 v-else-if="time<18">Good afternoon</h1>
    <h1 v-else>Good evening</h1>
  </div>
</template>

<style scoped>
h1{
  text-align: center;
}

</style>
