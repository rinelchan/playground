<script setup>
// array in v-for + v-if
const myRecipe= ([
  'Omelette',
  'Japanese curry',
  'Gyōza',
  'Salad'
])

const subjects = ['INT203', 'INT204', 'INT206', 'INT208']

const numbers = [1, 2, 3, 4, 5]

const students = [
  {
    studentID: 1,
    name: "Dominic Toretto",
  },
  {
    studentID: 2,
    name: "James Bond",
  },
  {
    studentID: 3,
    name: "Arthur Curry",
  }
]
</script>

<template>
  <ul>
      <li v-for="recipe in myRecipe" :key="recipe">{{ recipe }}</li>
  </ul>

  <ul>
      <li v-for ="(subject, index) in subjects" :key="index">
          {{ index }} - {{ subject }}
      </li>
  </ul>

  <!-- only numbers -->
  <ul>
    <li v-for="number in numbers" :key="number">
      <p v-if="number">
        <span>{{ number }}</span>
      </p>
    </li>
  </ul>

  <!-- only student name -->
  <ul>
   <li v-for="student in students" :key="student">
     <p v-if="student.name">
       <span>{{  student.name  }}</span>
     </p>
   </li>
  </ul>

</template>

<style scoped>

</style>