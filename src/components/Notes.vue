<template>

    <div class="grid gap-1 sm:grid-cols-2  md:grid-cols-4 lg:grid-cols-6 container mx-auto ">
    <Note v-for="n in 10" :key="n" />
    <NoteAdd/>
    </div>

<NotesForm v-if="show"/>
  
</template>

<script setup>
    import {show} from '~/helpers/useNotes'
</script>