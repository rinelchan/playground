<script setup>
//นำเลข1-9มาใส่ช่องได้ผลบวก15ทุกแนว
//https://www.youtube.com/watch?v=wn7OLfD28io
import {  ref  } from 'vue'
// const nums = ref([0,0,0,0,0,0,0,0,0,0,0,0,0,0])
// const nums = ref([1,2,3,4,5,6,7,8,9,10,11,12,13,14,15])
const nums = ref([1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1])
const numsAnswer = ref([3, 7, 11, 12, 13, 14])
const genNum = ref(3)
const message = ref("")
const isNotBound = (index) => index !=3 && index != 7 && index < 11
const sumOfDimension = (index, dimension) => {
  var sumValue = 0
  if (dimension === 'x') {
    for (var i = index - 3; i < index; i++) {
      sumValue += nums.value[i]
    }
  } else {
    for (var i = index - 12; i < index; i += 4) {
      sumValue += nums.value[i]
    }
  }
  nums.value[index] = sumValue
  return sumValue
}

const checkAnswer = () => {
  const isAnswer = numsAnswer.value.every(
    (index) => nums.value[index] === genNum.value
  )
  if (isAnswer) {
    message.value = "mission complete"
  } else if (nums.value === nums.value) {
    message.value = "duplicate number!!!"
  } else {
    message.value = "Nooooo!!!!"
  }
}

const reset = () => {
  nums.value = [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]
}

</script>

<template>
  <div class="top-container">
    <h1>นำเลข 1-9 มาใส่ช่องได้ผลบวก {{  genNum  }} ทุกแนว</h1>
    <div class="action-button">
      <input type="number" v-model="genNum" />
      <button @click="checkAnswer">Check</button>
      <button @click="reset">Reset</button>
    </div>
    <div class="grid-container">
        <!-- show input -->
        <div v-for="(num, index) in nums" :key="index">
          {{ index }}
        <!-- เป็นกล่องที่กรอกเลขได้ -->
        <span v-if="isNotBound(index)">
          <input class="input-item" type="number" v-model="nums[index]"/>
        </span>
        <!-- เป็นขอบ -->
        <span v-else>
          <!-- <input disabled class="input-item" v-model="nums[index]"/> -->
          <input 
            disabled 
            style="background-color: rgba(241, 195, 110, 0.8)" 
            class="input-item" 
            type="number"
            :value="sumOfDimension(index, index > 11 ? 'y' : 'x')" 
          />
        </span>
        </div>
      <div>
    </div>
  </div>
    <div class="complete-message">
        <!-- show message -->
        {{  message  }}
    </div>
  </div>
</template>

<style scoped>
.top-container {
  width: 430px;
}
.action-button {
  padding: 10px;
  display: flex;
  gap: 5px;
}
.grid-container {
  display: grid;
  grid-template-columns: 100px 100px 100px 100px;
  grid-template-rows: 80px 80px 80px 80px;
  column-gap: 5px;
  row-gap: 5px;
  background-color: green;
  padding: 10px;
}
.complete-message {
  height: 40px;
  font-size: 30px;
  color: rgb(43, 20, 246);
}
.input-item {
  display: flex;
  border: 1px solid rgba(0, 0, 0, 0.8);
  font-size: 30px;
  text-align: center;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  width: 70%;
}
</style>
