<template>
    <header class="sticky top-0  shadow-lg">
        <nav class="container flex flex-col sm:flex-row items-center gap-4 text-black py-6">
           <RouterLink :to="{ name: 'home' }">
            <div class="flex items-center gap-3">
                <i class="fa-solid fa-sun"></i>
                <p class="text-xl">SkyCast</p>
            </div>
           </RouterLink>
           <div class="flex gap-3 flex-1 justify-end">
            <i class="fa-solid fa-circle-info text-xl hover:text-secondary-color duration-150 cursor-pointer"
            @click="toggleModal"
            ></i>
            <i class="fa-solid fa-plus text-xl hover:text-secondary-color duration-150 cursor-pointer"></i>
        </div>

        <PopupModal 
        :modal-active="modalActive"
        @close-modal="toggleModal"
        >
            <div class="text-black">
          <h1 class="text-2xl mb-1">Overview</h1>
          <p class="mb-4">
           SkyCast is an application that enables you to monitor the current and future weather in cities of your choice.
          </p>
          <h2 class="text-2xl">How it works</h2>
          <ol class="list-decimal list-inside mb-4">
            <li>
                To track the weather in a city, type its name into the search bar and select it from the results.
            </li>
            <li>
                This will take you to the current weather for your selected city.
            </li>
            <li>
                To save a city for later viewing on the home page, click on the "+" icon in the top right and track the city.
            </li>
          </ol>

          <h2 class="text-2xl">Delete a city</h2>
          <p>
            If you no longer want to track a city, navigate to the home page, select the city, and click on the delete option at the bottom of the page.

          </p>
        </div>
        </PopupModal>
        </nav>
    </header>
</template>

<script setup>
import { ref } from "vue"
import { RouterLink } from 'vue-router';
import  PopupModal from './PopupModal.vue'

const modalActive = ref(null);
const toggleModal = () => {
    modalActive.value = !modalActive.value;
}
</script>

