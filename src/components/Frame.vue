<script setup lang="ts">
import { PropType } from "vue";
import { Animal } from "../enums.ts";

const {backgroundColor} = defineProps({
    chosenAnimal: String as PropType<Animal>,
    backgroundColor: String,

})

// const backgroundColor = `bg-${color}-${intensity}`;

</script>

<template>
    <div 
    :class="`${backgroundColor} drop-shadow-md shadow-lg rounded-sm p-4 flex justify-center w-3/4 mx-auto`"
   >
        <img 
        class="object-contain rounded-sm max-w-2xl max-h-[40rem]" :src="chosenAnimal" 
        alt="animal" />
    </div>
</template>

