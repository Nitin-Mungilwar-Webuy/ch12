<script setup>
import { ref, computed } from "vue";
// computed peoperty without ref
// let firstName = "nitin";
// let lastName = "mungilwar";

// const fullName = computed(() => {
// console.log("getter called");
//   return firstName + " " + lastName;
// });

// setTimeout(() => {
// console.log("getter called");
//   let firstName = "rekha";
//   console.log("sttimeout called");
// }, 3000);

//computed peoperty with ref
let firstName = ref("nitin");
let lastName = ref("mungilwar");

const fullName = () => {
  console.log("getter called");
  return firstName.value + " " + lastName.value;
};

setTimeout(() => {
  console.log("getter called");
  firstName.value = "rekha";
  console.log("sttimeout called");
}, 2000);
</script>
<template>
  {{ fullName() }}
</template>
<style></style>
