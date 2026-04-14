<template>
  <v-container>
    <h1><v-icon size="large" class="mb-2">mdi-calculator</v-icon> Calculator</h1>

    <v-radio-group v-model="operator" inline>
      <v-radio label="Addition" value="+"></v-radio>
      <v-radio label="Subtraction" value="-"></v-radio>
      <v-radio label="Multiplication" value="*"></v-radio>
      <v-radio label="Division" value="/"></v-radio>
    </v-radio-group>

    <v-card>
      <v-card-text>
        <h2>Selected Operator</h2>
        
        <v-text-field label="Enter 1st number" v-model.number="num1" type="number"></v-text-field>
        <v-text-field label="Enter 2nd number" v-model.number="num2" type="number"></v-text-field>
        <v-text-field label="Total" v-model="total"></v-text-field>
        <v-btn color="purple" class="mt-4" @click="calculate">Calculate</v-btn>


      </v-card-text>
    </v-card>
  </v-container>
</template> 

<script setup>

const num1 = ref(0)
const num2 = ref(0)
const total = ref(0)
const operator = ref()

function calculate() {

  if (operator.value === '+') {
    total.value = num1.value + num2.value
  } else if (operator.value === '-') {
    total.value = num1.value - num2.value
  } else if (operator.value === '*') {
    total.value = num1.value * num2.value
  } else if (operator.value === '/') {
    total.value = num1.value / num2.value
  }
}
</script>