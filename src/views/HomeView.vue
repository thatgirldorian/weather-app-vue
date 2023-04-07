<script setup></script>

<template>
    <main class="container text-black">
        <div class="pt-4 mb-8 relative">
            <input type="text" 
            v-model="searchQuery"
            placeholder="Look up a city or state :)"
            class="py-2 px-1 w-full bg-transparent border-b focus:border-secondary-color focus:outline-none focus:shadow-[0px_1px_0_0_#a8dadc]"
            >
        </div>
    </main>
</template>

<script>
import { ref } from "vue"

const searchQuery = ref("")
</script>
