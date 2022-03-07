<script setup>
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];
</script>
 
<template>
  <div>
    <ul>
      <li v-for ="(number, index) in numbers" :key="index">
        {{ number }}
      </li>
    </ul>
  </div>
</template>
 
<style>

</style>