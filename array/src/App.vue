<script setup>
const numbers = [1, 2, 3, 4, 5, 6, 7, 8];
const students = [
  {
    studentId: 1,
    name: "John Weak",
  },
  {
    studentId: 2,
    name: "Scott Tiger",
  },
  {
    studentId: 3,
    name: "Ethan Summer",
  },
];
const mixdata = [
  1,
  "text1",
  2,
  "text2",
  {
    studentId: 2,
    name: "Scott Tiger",
  },
  4,
];
</script>

<template>
<div>

 <!-- <ul>
   <li v-for="(number,index) in numbers" :key="index">
        {{ numbers }} - {{  students  }} <br>
   </li>
 </ul>

  <ul>
   <li v-for="(student,index) in students" :key="index">
        {{  students  }} <br>
   </li>
  </ul> -->

<!-- only id -->
   <ul>
   <li v-for="student in students" :key="student">
     <p v-if="student.studentId">
       {{  student.studentId  }} 
     </p>
   </li>
  </ul>

<!-- only name -->
  <ul>
   <li v-for="student in students" :key="student">
     <p v-if="student.name">
       <span>{{  student.name  }}</span>
     </p>
   </li>
  </ul>

<!-- all data student -->
  <ul>
    <li v-for="student in students" :key="student">
      <p v-if="student">
        <span>{{ student }}</span>
      </p>
    </li>
  </ul>

<!-- id + name student -->
  <ul>
    <li v-for="student in students" :key="student">
      <p v-if="student">
        <span>{{ student.studentId }} - {{ student.name}}</span>
      </p>
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


  <ul>
    <li v-for="(number,students) in numbers" :key="number">
      <p v-if="number">
        <span>{{ numbers }} - {{ students }}</span>
      </p>
    </li>
  </ul>


</div> 


</template>