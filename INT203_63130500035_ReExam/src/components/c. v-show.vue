<script setup>
const isPresent = true
const msg = ''
</script>
 
<template>
<!-- v-show -->
  <div>
    <p v-show="!isPresent">2021</p>
    <p v-show="isPresent">2022</p>
  </div>
 
  <p v-show="!msg">INT 203 Web-based Client Side Programming II </p>

  <span v-show="true">" Text is display "</span>
  <span v-show="false">" Text is not display "</span>
</template>
 
<style>

</style>