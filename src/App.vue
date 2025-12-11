<script setup>
import { reactive } from 'vue';
import Inputs from './components/Inputs.vue';
import Result from './components/Result.vue';
import Operations from './components/Operations.vue';

const estate = reactive({
  firstNum: 0,
  secondNum: 0,
  operators: ''
})

const firNumdigited = (event) => {
  estate.firstNum = event.target.value
}
const secNumdigited = (event) => {
  estate.secondNum = event.target.value
}

const StringOperation = () => {
  const { operators, firstNum, secondNum } = estate;
  switch (operators) {
    case 'somar':
      return `${firstNum} + ${secondNum} =`


    case 'subtrair':
      return `${firstNum} - ${secondNum} =`


    case 'multiplicar':
      return `${firstNum} * ${secondNum} =`


    case 'dividir':
      return `${firstNum} / ${secondNum} =`



  }

}

const makeOperation = () => {
  const { operators, firstNum, secondNum } = estate;
  switch (operators) {
    case 'somar':
      return Number(firstNum) + Number(secondNum);


    case 'subtrair':
      return Number(firstNum) - Number(secondNum);


    case 'multiplicar':
      return Number(firstNum) * Number(secondNum);


    case 'dividir':
      return Number(firstNum) / Number(secondNum);



  }

}

</script>


<template>
  <div class="container">
    <h1><span>Calc</span><span>Vue</span></h1>
    <div class="container-calc">
      <Inputs :fir-num-d="firNumdigited" :sec-num-d="secNumdigited" />

      <Operations :value="event => estate.operators = event.target.value" />

      <Result :operat-string="StringOperation()" :result="makeOperation()" />



    </div>
  </div>
</template>

<style scoped></style>
