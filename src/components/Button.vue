<script setup lang="ts">

</script>

<template>
    <button
        class="bg-orange-300 px-12 py-3 rounded-md text-2xl text-white font-bold shadow-sm drop-shadow-md hover:drop-shadow-sm duration-300 my-5"
        @click="$emit('flipImage')">
        Flip image
    </button>
</template>