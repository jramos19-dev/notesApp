<template>

    <div class="grid gap-1 sm:grid-cols-2  md:grid-cols-4 lg:grid-cols-6 container mx-auto ">
    <Note v-for="(note,index) in notes" :key="index" :note="note" @deleted="refresh"/>
    <NoteAdd/>
    </div>

<NotesForm v-if="show" @added="refresh" @saved="refresh"/>
  
</template>

<script setup>
    import {onMounted} from 'vue'
    import {show,notes,getAll} from '~/helpers/useNotes'

    onMounted (()=>refresh())

    const refresh = async() => await getAll()

</script>