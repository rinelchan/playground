<script setup>
import { ref, computed } from 'vue'
const numberInput = ref()
const runButton = ref()
const output = ref()

const multiplication = computed (() =>{
   for (let i = 0; i <= 12; i++) {
    sum = numberInput.value + ' x ' +  i  + ' = ' + (numberInput * i) + "<br>"
   }
   return sum
})

</script>
 
<template>
<div>
  <input type="number" v-model="numberInput" />
  <button @click="runButton" >ได้แก่</button>
  <span>{{ multiplication }}</span>
  <ul>
    <li v-for="(n, index) in 12" :key="index">
      {{  n  }} * {{ index }} = {{ n * index }}</li>
  </ul>
</div>

</template>
 
<style scoped>

</style>