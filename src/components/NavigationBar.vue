<template>
    <header class="sticky top-0  shadow-lg">
        <nav class="container flex flex-col sm:flex-row items-center gap-4 text-black py-6">
           <RouterLink :to="{name: 'home'}">
            <div class="flex items-center gap-3">
                <i class="fa-solid fa-sun"></i>
                <p class="text-xl">SkyCast</p>
            </div>
           </RouterLink>
           <div class="flex gap-3 flex-1 justify-end">
            <i class="fa-solid fa-circle-info text-xl hover:text-secondary-color duration-150 cursor-pointer"></i>
            <i class="fa-solid fa-plus text-xl hover:text-secondary-color duration-150 cursor-pointer"></i>
        </div>
        </nav>
    </header>
</template>

<script setup>
import { RouterLink } from 'vue-router';
</script>

