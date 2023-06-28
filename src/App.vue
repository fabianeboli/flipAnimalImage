<script setup lang="ts">
import { Animal } from './enums';
import Frame from "./components/Frame.vue"
import Button from "./components/Button.vue"
import { ref } from "vue";

const currentAnimal = ref<Animal>(Animal.Dog);

const flipImage = () => 
currentAnimal.value = currentAnimal.value === Animal.Dog
  ? Animal.Cat
  : Animal.Dog
</script>

<template>
  <Frame 
  background-color="bg-slate-50" 
  :chosen-animal="currentAnimal" />
  <Button 
  @flip-image="flipImage"/>
</template>

