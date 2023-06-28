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
    :class="`container ${backgroundColor} drop-shadow-md shadow-lg rounded-sm p-4 flex justify-center mx-auto`"
   >
        <img 
        class="object-contain rounded-sm max-w-xs sm:max-w-md md:max-w-lg xl:max-w-2xl max-h-[40rem]" :src="chosenAnimal" 
        alt="animal" />
    </div>
</template>

