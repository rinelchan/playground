<script setup>
const colorText = 'color: navy'
const decorateText = 'text-decoration: underline overline'
const imagePath = "../public/images/minion.png"
</script>
 
<template>
  <!-- v-bind -->
  <h1 v-bind:style="colorText">INT203 - ReExam</h1>
  <p :style="decorateText">63130500035</p>
  <img :src="imagePath">
</template>
 
<style>

</style>