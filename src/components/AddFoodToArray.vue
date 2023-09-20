<script setup>

import {ref} from "vue";

const Food = ref([]);

const inputFood = ref('')

function toAddFood(){
  Food.value.push(inputFood.value);
}

const filterArray = (food) =>{
  Food.value = Food.value.filter((removeFood) => removeFood !== food)
}

const randomItem = ref()

function randomNumber(){
  randomItem.value = Food.value[Math.floor(Math.random()*Food.value.length)]
}

</script>

<template>
  <div >
  <ol >
    <li v-for="food in Food" :key="food">
      {{food}}
      <button @click="filterArray(food)">Remove food</button>
    </li>
    <li id="input">
      <input type="text" v-model="inputFood"/>
    </li>
    <li id="input">
    </li>
    <li id="input">
      <button @click="toAddFood">Add new food</button>
      <button @click="randomNumber">Random</button>
    </li>
    <li id="input">
      <p>Here is random item: {{randomItem}}</p>
    </li>
  </ol>
  </div>
</template>

<style scoped>
li#input{
  list-style: none;
}
</style>
