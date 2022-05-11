<script setup>
import { ref } from 'vue'
const color = ref()
const fontSize = ref()
const checkAnswer = () => { alert(`color: ${color.value}, font-size: ${fontSize.value}`) }
const reset = () => { color.value = ref() , fontSize.value = ref()}
</script>

<template>
<!-- color selection -->
<select  v-model="color">
  <option disabled value="">select color</option>
  <option value="red" class="red">red</option>
  <option value="yellow" class="yellow">yellow</option>
  <option value="green" class="green">green</option>
  <option value="blue" class="blue">blue</option>
  <option value="purple" class="purple">purple</option>
  
</select>

<input type="color" v-bind:class="color" v-model="color"/>

<!-- font-size selection -->
  <select type="number" v-bind:class="fontSize" v-model="fontSize">
    <option disabled value="">select font-size</option>
    <option value="12 px" class="12"> 12 px </option>
    <option value="14 px" class="14"> 14 px </option>
    <option value="18 px" class="18"> 18 px </option>
    <option value="24 px" class="18"> 24 px </option>
    <option value="30 px" class="30"> 30 px </option>

  </select>

<!-- check + reset button -->
<br>
<button @click="checkAnswer">Check</button>
<button @click="reset">Reset</button>

</template>
 
<style scoped>
.red {
background-color: #E20A0A;
color: #ffffff;
}
.yellow {
background-color: #ffff02;
color: #000000;
}
.green {
background-color: #3CB371;
color: #ffffff;
}
.blue {
background-color: #00bfff;
color: #000000;
}
.purple {
 background-color: #4901ff;
color: #ffffff;
}

</style>