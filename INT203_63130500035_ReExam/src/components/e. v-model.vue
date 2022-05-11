<script setup>
import { ref, computed } from 'vue'
const side = ref(2)
const calculateArea = computed(() => side.value * side.value)

const text =ref('sleep')
</script>
 
<template>
<!-- v-model -->
  <h1>Square area</h1>
  <p> Side: <input type="number" v-model="side"></p>
  <p> Result: {{ calculateArea }}</p>

  <hr>

  <h1>Selection</h1>
  <select v-model="selected">
    <option disabled value="">choose one option.</option>
    <option> INT203 </option>
    <option> INT204 </option>
    <option> INT206 </option>
  </select>

  <hr>
           
  <input v-model="text">

</template>
 
<style></style>