<script setup>
import { ref, computed } from 'vue'
const number1 = ref()
const number2 = ref()
const sum = ref()

const calculate = computed(() => 
  number1.value + number2.value
);
</script>
 
<template>
<div>
  <input type = "number" v-model="number1"/> <br>
  <input type = "number" v-model="number2"/> <br>
  <button>calculate</button>
  <span>{{ calculate }}</span>

</div>

</template>
 
<style scoped>

</style>