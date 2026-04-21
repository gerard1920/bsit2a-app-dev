<template>
    <div>
        <h1> Calculate page</h1>
    </div>
    <v-radio-group v-model="operator" inline>
      <v-radio label="Addition" value="+"></v-radio>
      <v-radio label="Subtraction" value="-"></v-radio>
      <v-radio label="Multiplication" value="*"></v-radio>
      <v-radio label="Division" value="/"></v-radio>
    </v-radio-group>

    <v-card width="500">
        <v-card-text>
            <v-form>
                <v-text-field v-model="firstnumber" label="Enter 1st Number"></v-text-field>
                <v-text-field v-model="secondnumber" label="Enter 2nd Number"></v-text-field>
                <v-text-field v-model="total" label="Total : "></v-text-field>
                <v-btn color="primary" @click="calculate" block>calculate</v-btn>
            </v-form>
        </v-card-text>
    </v-card>


</template>

<script setup>
const firstnumber = ref();
const secondnumber = ref();
const total = ref(0);
const operator = ref();

function calculate () {
    total.value = Number(firstnumber.value) + Number(secondnumber.value);
    total.value = Number(firstnumber.value) - Number(secondnumber.value);
    total.value = Number(firstnumber.value) * Number(secondnumber.value);
    total.value = Number(firstnumber.value) / Number(secondnumber.value);



}
</script>