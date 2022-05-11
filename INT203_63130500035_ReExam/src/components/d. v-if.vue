<script setup>
const point = 70
const Math = [0, 1, 2]
</script>
 
<template>
<!-- v-if + v-else -->
  <h2> Point: {{ point }} </h2>
  <p v-if = "point>= 80" >Excellent</p>
  <p v-else-if = "point>= 50" >Very Good</p>

  <hr>

  <h2 v-if="true">Yes, can show text.</h2>
  <h2 v-if="false">No, can not show text.</h2>

  <hr>

  <h2 v-if="Math.random() > 0.5">Yes, more than 0</h2>

</template>
 
<style>

</style>