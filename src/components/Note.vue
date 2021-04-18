/* eslint-disable linebreak-style */
<template>
  <div class="bg-amber-200 rounded text-center text-fuchsia-900 p-2 space-y-2">
    <h3 class="text-2xl font-thin">
      {{ $props.note.title }}
    </h3>
    <p class="text-sm font-medium">
      {{ $props.note.content }}
    </p>
    <div class="flex justify-around">
      <button @click="editNote(note)" class="hover:bg-green-300">
        <flat-color-icons:edit-image />
      </button>

      <button @click="removeNote($props.note.id)" class="hover:bg-red-100">
        <flat-color-icons:delete-row />
      </button>
    </div>
  </div>
</template>

<script setup>
import { defineProps, defineEmit } from "vue"
import { remove, showToggle, noteToEdit } from "~/helpers/useNotes"

defineProps({
  note: Object,
  default: {
    id: 0,
    title: "",
    content: "",
  },
})

const emit = defineEmit(["deleted"])

const removeNote = async (id) => {
  await remove(id)
  emit("deleted")
}

const editNote = (note) => {
  noteToEdit.value = note
  showToggle()
}
</script>
