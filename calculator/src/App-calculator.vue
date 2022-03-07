<script setup>
import { ref, computed } from 'vue';
const num1 = ref();
const num2 = ref();
const sum = ref();

// const calculate = () => {
//   sum.value = num1.value + num2.value;
// };

const calculate = computed(() => 
  num1.value + num2.value
);

</script>
 
<template>
  <div>
    <input type="number" v-model="num1" /> <br>
    <input type="number" v-model="num2" /> <br>
    <!-- <button @click="calculate">calculate</button>
    <span v-show="sum !== 0">{{ sum }}</span> -->
    <span>{{ calculate }}</span>
  </div>
</template>
 
<style>

</style>