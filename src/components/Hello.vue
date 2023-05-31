<!-- methods -->
<script setup>
import { ref, computed } from "vue";

// //without ref
// let firstName = "nitin";
// let lastName = "mungilwar";

// // method
// function fullName() {
//   return firstName + " " + lastName;
// }
// // const fullNam = () => {
// //   return firstName + " " + lastName;
// // };

// setTimeout(() => {
//   console.log("settimeout called");
//   firstName = "omsai";
// }, 2000);

//with ref
let firstName = ref("nitin");
let lastName = ref("mungilwar");

// method
function fullName() {
  return firstName.value + " " + lastName.value;
}
// const fullNam = () => {
//   return firstName + " " + lastName;
// };

setTimeout(() => {
  console.log("settimeout called");
  firstName.value = "omsai";
}, 2000);
</script>
<template>
  {{ fullName() }}<br />
  <!-- {{ fullNam() }} -->
</template>
<style></style>
