<template>

    <div class="text-gray-100 text-xl bg-amber-900 absolute inset-0 w-screen h-screen flex justify-center  items-center ">
        <button @click="showToggle" class=" absolute top-2 left-2">
            <mdi:close-circle-outline class="text-6xl"/>

        </button>
        <form @submit.prevent>
            <div class="flex flex-col">
                <label for="title" class="mb-2 text-amber-300 text-2xl">Title</label>
                <input type="text" name="title" class="rounded " placeholder="Title"/>
            </div>
            <div class="flex flex-col">
                <label for="content" class="mb-1 text-2xl text-amber-300">Content</label>
                <textarea name="content" class="rounded" placeholder="note content"/>
            </div>
            <div>
                <button class="w-full bg-orange-600 text-amber-900 p-2 rounded mt-3 hover:bg-orange-400 hover:text-blueGray-600 ">
                    Add Note
                </button>
            </div>

        </form>
    </div>
</template>

<script setup>
    import {showToggle } from '~/helpers/useNotes'
</script>