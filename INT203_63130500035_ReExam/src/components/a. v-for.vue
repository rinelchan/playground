<script setup>
const cartoons = ['minion', 'doraemon','kitty','shin-chan','we-bare-bears']

const subject = [
  {
  ID: 'INT203',
  Name: 'Web-based Client Side Programming II' 
  },
  {
  ID: 'INT204',
  Name: 'Web-based Server Side Programming II'
  },
  {
  ID: 'INT206',
  Name: 'Advanced Database'
  },
  {
  ID: 'INT208',
  Name: 'Network II'
  }
] 

const product = {
    productId: '035',
    productName: 'Notebook',
    productPrice: '45000' 
}

</script>
 
<template>
  <!-- v-for -->
  <ul>
    <li v-for="cartoon in cartoons" :key="cartoon">{{ cartoons }}</li>
  </ul>

  <ul>
      <li v-for ="(cartoon, index) in cartoons" :key="index">
          {{ index }}: {{ cartoon }}
      </li>
  </ul>

  <ul>
      <li v-for="(value) in subject" :key="value">
          Semester 2 / 2022 : {{ value }}
      </li>
  </ul>

  <ul>
      <li v-for="(value, number) in product" :key="number">
          {{ product.productId }} - {{ number }}: {{ value }}
      </li>
  </ul>
</template>
 
<style>

</style>