<template>
    <div class=" bg-amber-200 rounded justify-center  text-center p-2 space-y-2 flex items-center  text-fuchsia-900 ">
        <button @click="showToggle" class="text-6xl transform transition-all hover:scale-125  hover:text-green-500 text-green-300">
        <ic:outline-add-circle-outline/> 
        </button>
    </div>
</template>

<script setup>
    import {showToggle } from '~/helpers/useNotes'
</script>