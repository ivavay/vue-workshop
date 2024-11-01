<template>
  <div>
    <h1>{{ count }}</h1>
    <!-- This creates a two-way binding: any changes to the input field will update the countby value
and any changes to the countby value will update the input field. -->
    <input v-model="countby" type="number" />
    <!-- The label is passed down to the button child component -->
    <!-- The @click-event listens for an event emitted by the child button component -->
    <Button label="Increment" @click-event="incrementCount" />
    <!-- TODO: Write a button for decrement -->
    <!-- Your code here ✨-->

    <Button label="Change Countby to 5" @click-event="changeCountby" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Button from './Button.vue';

const count = ref(0)
const countby = ref(1)

function changeCountby() {
  countby.value = 5 // Change the countby value programmatically
}

function incrementCount() {
  count.value += countby.value
}
// TODO: Write a decrementCount function 
function decrementCount() {
  // Your code here ✨

}
</script>


<style scoped>
h1 {
  color: #35495e;
  font-size: 110px;
}

input {
  font-size: 20px;
  padding: 10px;
  margin: 10px;
  width: 40px;
}
</style>