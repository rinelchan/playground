<script setup>
import { ref } from 'vue'
const count = ref(0)

const side = ref(2)
const area = ref()
const computeArea = () => { area.value = side.value * side.value }

const clickAlert = () => { alert("Hello! This is alert box.") }
</script>

<template>
  <h3>Count ++</h3>
  <button v-on:click="count++"> Add 1 + </button>
  <button v-on:click="count--"> Reduce 1 - </button>
  Count is: {{ count }}

  <hr>

  <h3>Square Area</h3>
  <p>Side: {{ side }}</p>
  <button v-on:click="side++">Add 1 Side +</button>
  <button v-on:click="side--">Reduce 1 Side -</button>

  <p>Area : {{ area }}</p>
  <button v-on:click="computeArea">Compute Area</button>

  <hr>

  <h3>Alert Box</h3>
  <button v-on:click="clickAlert()">Try Alert</button>

</template>

<style scoped>

</style>