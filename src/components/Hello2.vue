<script setup>
import { ref, computed } from "vue";
// computed peoperty without ref
let firstName = "nitin";
let lastName = "mungilwar";

const fullName = computed(() => {
  return firstName + " " + lastName;
});

setTimeout(() => {
  let firstName = "rekha";
  console.log("sttimeout called");
}, 3000);
</script>
<template>
  {{ fullName }}
</template>
<style></style>
